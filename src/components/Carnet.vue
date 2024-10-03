<script  >
import Field from './Field.vue';

export default {
    components:{
       Field},
    data() {
      return {
        flagSrc: "/chile_bandera.png",
        photoSrc: "/foto_elon.jpg",
        run: "22.222.222-2",
        lastName: "MUSK",
        firstName: "ELON REEVE",
        nationality: "SUDAFRICANO",
        sex: "M",
        birthDate: "28 JUN 1971",
        documentNumber: "222.222.222",
        issueDate: "01 ENE 2025",
        expiryDate: "01 ENE 2030",
        signature: "X Æ A-12"
      };
    }
  };
</script>

<template>
     <div class="carnet">
      <aside>
        <div>
          <span>CEDULA DE INDENTIDAD</span>
          <img width="40" src="../../public/chile_bandera.png" alt="" />
        </div>
        <img src="/foto_elon.jpg" alt="" />
        <p>RUN {{ run }} </p>
      </aside>

      <main>
        <header>
          <p>REPUBLICA DE CHILE</p>
          <span>SERVICIO DE REGISTRO CIVIL E IDENTIFICACIÓN</span>
        </header>
        <section>
            <Field title="APELLIDOS" :valor="lastName" />
            <Field title="NOMBRES" :valor="firstName"/>
          <div class="grid-2-colums">
            <Field title="NACIONALIDAD" :valor="nationality"/>
            <Field title="SEXO" :valor="sex"/>
          </div>
          <div class="grid-2-colums">
            <Field title="FECHA DE NACIMIENTO" :valor="birthDate"/>
            <Field title="NÙMERO DOCUMENTO" :valor="documentNumber"/>
          </div>
          <div class="grid-2-colums">
            <Field title="FECHA DE EMISIÒN" :valor="issueDate"/>
            <Field title="FECHA DE VENCIMIENTO" :valor="expiryDate"/>
          </div>
          <Field title="FIRMA DEL TITULAR" :valor="signature"/>
        </section>
      </main>
    </div>
</template>

<style scoped>
    .carnet{
    width: 400px;
    height: 230px;
    background: #c8deed;
    border-radius: 20px;
    display: grid;
    grid-template-columns: 30% 1fr;
    padding: 15px;
    box-shadow: 0px 0px 10px 2px black;
    }
</style>
