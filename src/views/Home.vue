<template>
  <div class="home">
    <p>my name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click Me</button>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  setup() {

    let name = 'mario'
    let age = 30

    const handleClick = () => {
      console.log('You clicked me')
    }

    return{ name, age, handleClick }
  }
  
}
</script>
