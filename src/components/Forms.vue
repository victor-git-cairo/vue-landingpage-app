<template>
    <div class="hero-box-right">
        <form method="post" action="#">
          <input-text role="first-name" label="First Name"></input-text>

          <input-text role="last-name" label="Last Name"></input-text>

          <input-text role="email" label="Email"></input-text>

          <form-button label="Contact Us"></form-button>
        </form>
      </div>
</template>

<script>
import InputText from "./InputText";
import FormButton from "./Button";

export default {
  name:"Forms",
  components:{
    InputText,
    FormButton
  }

}
</script>