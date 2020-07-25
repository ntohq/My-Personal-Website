<template>
   <section class="section">
     <slot/>
     <h2 class="title is-2 has-text-centered">Contact Form</h2>
     <b-field label="Name">
      <b-input :value="formName"></b-input>
    </b-field>

    <b-field label="Email">
      <b-input type="email"
        placeholder="youremail@example.com"
        maxlength="30"
        :value="formEmail">
      </b-input>
    </b-field>

    <b-field label="Subject">
      <b-input
        maxlength="30" :value="formSubject">
      </b-input>
    </b-field>

    <b-field label="Body">
      <b-input minlength="20" maxlength="200" type="textarea" :value="formBody"></b-input>
    </b-field>

    <b-button v-on:click="submitForm" type="is-primary" size="is-medium">Submit</b-button>
   </section>
</template>