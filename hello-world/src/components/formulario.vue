<template>
  <div class="container bg-light">
    <div class="row"> 
       <form action="" method="post">
          
          <div class="col-md-3"><label for="name">Nome</label>
          </div>
          <div class="col-md-6">
            <input type="text" class="form-control" id="name" name="name" aria-describedby="name" placeholder="Digite seu nome" v-model="nome">
          </div>

          <div class="col-md-3">
            <label for="exampleInputEmail1">Email address</label>
          </div>
          <div class="col-md-6">
            <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email" v-model="email">
          </div>
            <input type="submit" class="btn btn-primary mt-3" value="Enviar">
          <div class="col-md-4 mt-5">
             <p>Nome: {{ nome }}</p>  
            <p>E-mail: {{ email }}</p>
          </div>
  
    </form>
</div>
</div>

    
   


</template>

<script>
export default{
 data() {
  return {
      nome: '',
       email: '',
    };

   }
 
}
</script>

<style>

</style>