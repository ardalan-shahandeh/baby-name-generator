<script setup lang="ts">
enum Gender {
  GIRL = "Girl",
  BOY = "Boy",
  UNISEX = "Unisex",
}

enum Popularity {
  TRENDY = "Trendy",
  UNIQUE = "Unique",
}

enum Length {
  LONG = "Long",
  SHORT = "Short",
  ALL = "All",
}

interface OptionsState {
  gender: Gender;
  popularity: Popularity;
  length: Length;
}

const options = reactive<OptionsState>({
  gender: Gender.GIRL,
  length: Length.SHORT,
  popularity: Popularity.TRENDY,
});

function setLength(value: string) {
  options.length = value;
}

function setGender(value: string) {
  options.gender = value;
}

function setPopularity(value: string) {
  options.popularity = value;
}
</script>

<template>
  <div class="container">
    <h1>Baby Name Generator</h1>
    <p>Choose your options and click the "Find Name " buttom below</p>
    <div class="options-container">
      <div class="option-container">
        <h4>1) Choose a gender</h4>

        <div class="option-buttons">
          <button
            class="option"
            :class="options.gender === Gender.BOY && 'option-active'"
            @click="setGender(Gender.BOY)"
          >
            Boy
          </button>

          <button
            class="option"
            :class="options.gender === Gender.UNISEX && 'option-active'"
            @click="setGender(Gender.UNISEX)"
          >
            Unisex
          </button>

          <button
            class="option"
            :class="options.gender === Gender.GIRL && 'option-active'"
            @click="setGender(Gender.GIRL)"
          >
            Girl
          </button>
        </div>
      </div>

      <div class="option-container">
        <h4>2) Choos the name's popularity</h4>

        <div class="option-buttons">
          <button
            class="option"
            :class="options.popularity === Popularity.TRENDY && 'option-active'"
            @click="setPopularity(Popularity.TRENDY)"
          >
            Trendy
          </button>

          <button
            class="option"
            :class="options.popularity === Popularity.UNIQUE && 'option-active'"
            @click="setPopularity(Popularity.UNIQUE)"
          >
            Unique
          </button>
        </div>
      </div>

      <div class="option-container">
        <h4>3) Choos name length</h4>

        <div class="option-buttons">
          <button
            class="option"
            :class="options.length === Length.LONG && 'option-active'"
            @click="setLength(Length.LONG)"
          >
            Long
          </button>

          <button
            class="option"
            :class="options.length === Length.ALL && 'option-active'"
            @click="setLength(Length.ALL)"
          >
            All
          </button>

          <button
            class="option"
            :class="options.length === Length.SHORT && 'option-active'"
            @click="setLength(Length.SHORT)"
          >
            Short
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  font-family: Arial, Helvetica, sans-serif;
  color: rgb(27, 60, 138);
  max-width: 50rem;
  margin: 0 auto;
  text-align: center;
}

.container h1 {
  font-size: 3rem;
}

.options-container {
  background-color: rgb(255, 238, 236);
  border-radius: 2rem;
  padding: 1rem;
  width: 95%;
  margin: 0 auto;
  margin-top: 4rem;
  position: relative;
}

.option-container {
  margin-bottom: 2rem;
}

.option-buttons .option:first-child {
  border-radius: 1rem 0 0 1rem;
}

.option-buttons .option:last-child {
  border-radius: 0 1rem 1rem 0;
}

.option {
  background-color: white;
  outline: 0.15rem solid rgb(249, 87, 89);
  border: none;
  padding: 0.75rem;
  width: 12rem;
  font-size: 1rem;
  color: rgb(27, 60, 138);
  cursor: pointer;
  font-weight: 300;
}

.option-active {
  background-color: rgb(249, 87, 89);
  color: white;
}
</style>

function reactive(arg0: { gender: string; popularity: string; length: string; })
{ throw new Error("Function not implemented."); } function reactive(arg0: {
gender: string; popularity: string; length: string; milk: boolean; }) { throw
new Error("Function not implemented."); }
