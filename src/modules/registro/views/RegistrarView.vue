<template>
    <div>
        <h2>Formulario de registro</h2>
        <Form :validation-schema="schema" @submit="onSubmit">
            <div class="form">
                <label for="nombre">Nombre:</label>
                <Field type="text" name="nombre" id="nombre" placeholder="ingrese su nombre" />
                <ErrorMessage name="nombre"></ErrorMessage>
            </div>
            <div class="form">
                <label for="correo">Correo:</label>
                <Field type="email" name="email" id="correo" placeholder="ingrese su correo" />
                <ErrorMessage name="email"></ErrorMessage>
            </div>
            <button type="submit">Registrar</button>
        </Form>
    </div>
</template>
<script setup>


import {Form, Field, ErrorMessage} from 'vee-validate';
import {schema} from '../schemas/validationSchema'
import { errorMessages } from 'vue/compiler-sfc';


const onSubmit = () => {
    console.log('Se ha enviado el formulario');
}
</script>
<style scoped>
.form{
    margin-bottom: 10px;
}
</style>