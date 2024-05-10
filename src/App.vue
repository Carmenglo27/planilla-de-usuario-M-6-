<template>
 <div class="container border rounded">
  <form>
<div class="mb-3" >
 <label class="form-label"><strong>Nombre</strong></label>
 <input class="form-control" v-model="usuario.nombre" />
</div>
<div class="mb-3">
 <label class="form-label"> <strong>Nacionalidad</strong></label>
 <select class="form-select" v-model="usuario.nacionalidad">
 <option value="chile">Chile</option>
 <option value="extranjero"><strong>Extranjero</strong></option>
 </select>
</div>
<div class="mb-3">
 <label class="form-label"><strong>Genero</strong></label>
 <div class="d-flex gap-3">
 <div class="form-check">
 <input
 class="form-check-input" type="radio" name="flexRadioDefault"
 id="m" value="m" v-model="usuario.genero"
 />
 <label class="form-check-label fw-normal" for="m">
 Masculino
 </label>
 </div>
 <div class="form-check">
 <input
 class="form-check-input" type="radio" name="flexRadioDefault"
 id="f" value="f" v-model="usuario.genero"
 />
 <label class="form-check-label fw-normal" for="f"> Femenino </label>
 </div>
 </div>
</div>
<div class="mb-3">
 <label class="form-label"><strong>Direccion de residencia</strong></label>
 <input class="form-control" v-model="usuario.direccion" />
</div>

<div class="mb-3">
 <label class="form-label"><strong>Estado Civil</strong></label>
 <div class="d-flex gap-3">
 <div class="form-check">
 <input
 class="form-check-input" type="radio" name="flexRadioDefault"
 id="s" value="s" v-model="usuario.estadoCivil"/>
 <label class="form-check-label fw-normal" for="s">
 Soltero
 </label>
 </div>
 <div class="form-check">
 <input
 class="form-check-input" type="radio" name="flexRadioDefault"
 id="c" value="c" v-model="usuario.estadoCivil"
 />
 <label class="form-check-label fw-normal" for="c"> Casado </label>
</div>
</div>
</div>

<div class="mb-3">
  <label><strong>Continentes que ha visitado</strong> </label>
  <div class="d-flex gap-3">
    <ul>
  <input v-model="continentes" name="continentes" type="checkbox" value="America" />
America
  <input v-model="continentes" name="continentes" type="checkbox" value="Europa" />
Europa 
  <input v-model="continentes" name="continentes" type="checkbox" value="Asia" />
Asia
  <input v-model="continentes" name="continentes" type="checkbox" value="Africa" />
Africa
  <input v-model="continentes" name="continentes" type="checkbox" value="Oceania" />
Oceania
  </ul>
</div>
{{ continentes }}
</div>
</form>

<div class="planilla text-center mt-5 w-75 mx-auto">
<h1>Planilla de Usuario</h1>
<hr />
<table class="table table-striped">
 <thead>
 <tr>
 <th>Nombre</th>
 <th>Nacionalidad</th>
 <th>Género</th>
 <th>Direccion</th>
 <th>Estado Civil</th>
 <th>Continentes que ha visitado</th>
 </tr>
 </thead>
 <tbody>
 <tr>
 <td>{{ usuario.nombre }}</td>
 <td>{{ usuario.nacionalidad }}</td>
 <td>{{ usuario.genero }}</td>
 <td>{{ usuario.direccion}}</td>
 <td>{{ usuario.estadoCivil}}</td>
 <td>{{ continentes}}</td>
 </tr>
 </tbody>
</table>
</div>
</div>
  
</template>

<script>
export default {
name: "App",
data() {
 return {
 usuario: {
 nombre: "",
 nacionalidad: "",
 genero: "",
 direccion:"",
 estadoCivil:"",
 continentes: "[]",
 },
 };
},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
