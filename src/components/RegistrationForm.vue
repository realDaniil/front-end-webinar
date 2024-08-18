<template>
  <Form
    @submit="onSubmit"
    :validation-schema="schema"
    class="registration-form"
  >
    <p class="top-text">
      Запишитесь <span style="color: #ff3459">бесплатно</span> и получите
      подарок
    </p>

    <div class="form-group">
      <Field name="name" v-slot="{ field, errorMessage }">
        <input
          class="input"
          v-bind="field"
          type="text"
          placeholder="Ваше имя и фамилия"
        />
        <span v-if="errorMessage" class="error">{{ errorMessage }}</span>
      </Field>
    </div>
    <div class="form-group">
      <Field name="phone" v-slot="{ field, errorMessage }">
        <VueTelInput
          v-bind="field"
          v-model="phone"
          :preferred-countries="['ua']"
          :default-country="defaultCountry"
          placeholder="Ваш номер телефона"
          @blur="field.blur"
          @input="onPhoneInput"
          @country-changed="onCountryChanged"
          class="phone input"
        />
        <span v-if="errorMessage" class="error">{{ errorMessage }}</span>
      </Field>
    </div>
    <div class="form-group">
      <Field name="email" v-slot="{ field, errorMessage }">
        <input
          class="input"
          v-bind="field"
          type="email"
          placeholder="Ваш email"
        />
        <span v-if="errorMessage" class="error">{{ errorMessage }}</span>
      </Field>
    </div>
    <button type="submit">Записаться бесплатно</button>
    <p class="bottom-text">
      Нажимая на кнопку, я соглашаюсь
      <span style="text-decoration: underline; cursor: pointer">
        с политикой конфиденциальности
      </span>
    </p>
  </Form>
</template>

<script setup>
import { ref } from "vue";
import { Form, Field } from "vee-validate";
import * as yup from "yup";
import { VueTelInput } from "vue-tel-input";

const phone = ref("");
const defaultCountry = ref("ua");

const onPhoneInput = (event) => {
  phone.value = event.target.value;
};

const onCountryChanged = (countryData) => {
  const dialCode = countryData.dialCode;
  const phoneWithoutCode = phone.value.replace(/^\+?[0-9]*/, "");
  phone.value = `+${dialCode}${phoneWithoutCode}`;
};

const onSubmit = (values) => {
  window.location.reload();
};


const schema = yup.object({
  name: yup.string().required("Поле обязательно для заполнения"),
  phone: yup
    .string()
    .required("Поле обязательно для заполнения")
    .matches(/^\+?[0-9\s\-()]{7,17}$/, "Введите корректный номер телефона"),
  email: yup
    .string()
    .email("Введите корректный email")
    .required("Поле обязательно для заполнения"),
});

</script>

<style lang="scss">
.vue-tel-input {
  position: relative;
}
.vti__dropdown {
  z-index: 1;
}
.vti__input.vti__phone {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  width: 170px;
  z-index: 0;
}

.vue-tel-input.phone {
  background: #272d3d;
  color: #d7d7d7;
  * {
    color: #d7d7d7;
    background-color: #272d3d;
  }
}
</style>

<style scoped lang="scss">
.error {
  color: #ff3459;
  font-size: 12px;
  line-height: 0;
}
.registration-form {
  padding: 50px 60px;
  width: 370px;
  box-sizing: border-box;
  background: #303a53;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.top-text {
  margin-bottom: 20px;
  font-size: 22px;
  font-weight: 700;
  line-height: 25.99px;
  text-align: center;
}

.form-group {
  margin-bottom: 14px;
}

.input {
  background: #272d3d;
  border-radius: 5px;
  font-style: normal;
  font-weight: 400;
  font-size: 13px;
  line-height: 24px;
  color: #d7d7d7;
  border: none;
  outline: none;
  padding: 14px 22px;
  width: 250px;
  max-height: 52px;
  box-sizing: border-box;

  &:focus {
    box-shadow: inset 0 1px 1px #00000013, 0 0 8px #66afe999;
    border-color: #66afe9;
  }
}

button {
  box-sizing: border-box;
  cursor: pointer;
  background: #ff3459;
  border-radius: 5px;
  font-weight: 700;
  font-size: 15px;
  line-height: 24px;
  color: #d7d7d7;
  border: none;
  outline: none;
  padding: 14px 22px;
  width: 250px;
  margin-bottom: 14px;
  transition: 0.2s;

  &:hover {
    opacity: 0.8;
  }
}
.bottom-text {
  font-weight: 500;
  font-size: 12px;
  line-height: 150%;
  text-align: center;
  color: rgba(255, 255, 255, 0.5);
}

@media (max-width: 850px) {
  button {
    background: #0048ff;
  }
}
</style>
