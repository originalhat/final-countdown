<template>
  <div class="hello">
    <h1>Final Countdown</h1>
    <h2>How much time do you have left?</h2>

    <div class="age">
      <input class="age-input" id="age" type="number" placeholder="47" v-model="age">
      <label class="age-label" for="age"><span>}</span>age</label>
    </div>

    <div class="percentage">
      <span class="percentage-age">{{ Math.floor((age / 79) * 100) }}%</span>
      <!--<span class="percentage-label"><span>}</span>complete</span>-->
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      age: 47
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

.age {
  padding: 36px;
  margin-left: 72px; /* TODO: better way center align left column? */
}

.age-input {
  border: none;
  border-bottom: 1px solid #e3e3e3;
  border-radius: 2px;
  font-size: 24px;
  line-height: 24px;
  padding: 8px;
  text-align: center;
  width: 64px;
}

.age-label {
  font-size: 24px;
  line-height: 24px;
}

.age-label span {
  color: #e0e0d0;
  font-weight: 800;
  padding: 16px;
}

.percentage {
  padding: 36px;
}

.percentage-age {
  font-size: 48px;
  line-height: 48px;
}

.percentage-label{
  font-size: 48px;
  line-height: 48px;
}

.percentage-label span {
  color: #e0e0d0;
  font-weight: 800;
  padding: 16px;
}

a {
  color: #42b983;
}
</style>
