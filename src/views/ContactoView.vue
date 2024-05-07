<template>
    <!-- Page Header Start -->
    <div class="container py-5 px-2 bg-primary">
        <div class="row py-5 px-4">
            <div class="col-sm-6 text-center text-md-left">
                <h1 class="mb-3 mb-md-0 text-white text-uppercase font-weight-bold">Contacto</h1>
            </div>
            <div class="col-sm-6 text-center text-md-right">
                <div class="d-inline-flex pt-2">
                    <h4 class="m-0 text-white">
                        <RouterLink to="/" class="text-white">Inicio</RouterLink>
                    </h4>
                    <h4 class="m-0 text-white px-2">/</h4>
                    <h4 class="m-0 text-white">Contacto</h4>
                </div>
            </div>
        </div>
    </div>
    <!-- Page Header End -->

    <!-- Contact Start -->
    <div class="container bg-white pt-5">
        <div class="row px-3 pb-2">
            <div class="col-sm-4 text-center mb-3">
                <i class="fa fa-2x fa-globe mb-3 text-primary"></i>
                <h4 class="font-weight-bold">WebSite</h4>
                <p>https://github.com/Caat126</p>
            </div>
            <div class="col-sm-4 text-center mb-3">
                <i class="fa fa-2x fa-phone-alt mb-3 text-primary"></i>
                <h4 class="font-weight-bold">Phone</h4>
                <p>+59168317322</p>
            </div>
            <div class="col-sm-4 text-center mb-3">
                <i class="far fa-2x fa-envelope mb-3 text-primary"></i>
                <h4 class="font-weight-bold">Email</h4>
                <p>caarguedas126@gmail.com</p>
            </div>
        </div>
        <div class="col-md-12 pb-5">
            <div class="contact-form">
                <div v-show="enviado == true" class="alert alert-success">Mensaje enviado correctamente</div>

                <div class="control-group">
                    <input type="text" v-model="nombre" class="form-control" id="name" placeholder="Ingresa tu nombre completo" required="required"
                        data-validation-required-message="Please enter your name" />
                    <p class="help-block text-danger"></p>
                </div>
                <div class="control-group">
                    <input type="email" v-model="correo" class="form-control" id="email" placeholder="Ingresa tu correo" required="required"
                        data-validation-required-message="Please enter your email" />
                    <p class="help-block text-danger"></p>
                </div>
                <div class="control-group">
                    <input type="text" v-model="tema" class="form-control" id="subject" placeholder="Escribe el tema" required="required"
                        data-validation-required-message="Please enter a subject" />
                    <p class="help-block text-danger"></p>
                </div>
                <div class="control-group">
                    <textarea v-model="mensaje" class="form-control" rows="8" id="message" placeholder="Escribe tu mensaje" required="required"
                        data-validation-required-message="Please enter your message"></textarea>
                    <p class="help-block text-danger"></p>
                </div>
                <div>
                    <button class="btn btn-primary" @click="enviarMensaje()" type="button" id="sendMessageButton">Enviar mensaje</button>
                </div>
            </div>
        </div>
    </div>
    <!-- Contact End -->

</template>

<script>
import { ref } from 'vue';
import Axios from 'axios';

export default {

    setup() {

        const baseUrl = 'http://BlogTest.test/api';

        const enviado = ref(false);
        const nombre = ref('');
        const correo = ref('');
        const tema = ref('');
        const mensaje = ref('');

        const enviarMensaje = async () => {
            if (nombre.value == '' || correo.value == '' || tema.value == '' || mensaje.value == '') {
                alert ('Todos los campos son obligatorios');
                return;
            }
            try {
                const { data } = await Axios.post(baseUrl + '/contactos', {
                    nombre: nombre.value,
                    correo: correo.value,
                    tema: tema.value,
                    mensaje: mensaje.value
                }, {
                    headers: {
                        'Accept': 'application/json',
                        'Content-Type': 'application/json'
                    }
                });

            console.log(data);
            enviado.value = true;
            setTimeout(() => {
                enviado.value = false;
                nombre.value = '';
                correo.value = '';
                tema.value = '';
                mensaje.value = '';
            }, 2000)

            } catch (error) {
                console.log(error);
            }
        }

        return {
            enviado,
            nombre,
            correo,
            tema,
            mensaje,
            enviarMensaje
        }
    }
}
</script>

<style></style>