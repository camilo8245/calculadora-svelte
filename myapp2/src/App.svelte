<script>
  let numero1=0
  let numero2=0 
  let eleccion=0
  let total=0

  // function operar(){
  //   if (eleccion==1){
  //     total=numero1+numero2
  //   }

  //   if (eleccion==2){
  //     total=numero1-numero2
  //   }

  //   if (eleccion==3){
  //     total=numero1*numero2
  //   }

  //   if (eleccion==4){
  //     total=numero1/numero2
  //   }
  // }

  $:{

    if (eleccion==1){
      total=numero1+numero2
    }

    if (eleccion==2){
      total=numero1-numero2
    }

    if (eleccion==3){
      total=numero1*numero2
    }

    if (eleccion==4){
      total=numero1/numero2
    }
  }
    


</script>

<main>
  <h1>CALCULADORA MACKIA</h1>

  <select bind:value={eleccion}>
    <option value="0" >Seleccione una operacion</option>
    <option value="1" >Sumar</option>
    <option value="2" >Restar</option>
    <option value="3">Multiplicar</option>
    <option value="4">Dividir</option>
  </select><br/>

  <input class="fondoverde" type="number" bind:value={numero1} />
  <br/>
  <input type="number" bind:value={numero2} />
  <br/>
  
  <!-- <button on:click={operar}>Calcule</button> -->
  <br/>
  {#if eleccion==0}
  <span>Debe seleccionar una operacion</span>
  {:else}
  <div>El resultado de su operacion es:{total}</div>
  {/if}

<span> Hola Mundo by esbgo97</span>
  
  
</main>

<style>
  /* button{
    background-color: aqua;
    font-size: 50px;
    border-color: blue;

  } */

  input{
    background-color:darkorange;
    font-size: 20px;
    border-color: red;
  }

  .fondoverde{
    background-color: green;
  }

</style>
