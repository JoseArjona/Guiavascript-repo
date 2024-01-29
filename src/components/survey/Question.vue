<script setup lang="ts">
import { ref  } from 'vue';

interface Question {
  id: string;
  statement: string;
  answers: {
    id: string;
    answer: string;
    value: string;
    note: string;
  }[];
}
interface Props {
  question: Question;
}

const { question } = defineProps<Props>()

const answers = question.answers;

let successText  = ref('✨ Correcto: ');
let errorText = ref('❌ Incorrecto: ');
const currentValue = ref<string | null>(null);

const showNote = async (note:string) => {
  if (currentValue.value === "correct"){
    successText.value = '✨ Correcto: '+note
    errorText.value = ''; 
  } else{
    errorText.value = '❌ Incorrecto: '+note
    successText.value = '';
  }
}

</script>

<template>
  <article class="form flex f-col" >
    <p>{{ question.statement }}</p>
    <div v-for="answer in answers" :key="answer.id">
      <input type="radio" :id="'answer-' + question.id + '-' + answer.id" name="value-radio" :value="answer.value"
        @change="showNote(answer.note)" v-model="currentValue"/>
      <label :for="'answer-' + question.id + '-' + answer.id">{{answer.answer}}</label>
    </div>
    <span class="result success" >{{successText}}</span>
    <span class="result error" >{{errorText}}</span>
  </article>
</template>

<style>
p {
    margin: 0;
  }
  .form {
    display: flex;
    flex-direction: column;
    padding: 12px;
  }
  .form input {
    display: none;
  }
  .form label {
    display: flex;
    background-color: #d1cbcb;
    padding: 14px;
    margin: 8px 0 0 0;
    font-size: 0.82em;
    font-weight: 600;
    border-radius: 10px;
    cursor: pointer;
    border: 1px solid rgba(187, 187, 187, 0.164);
    color: #000;
    transition: 0.3s ease;
  }

  .form label:hover {
    background-color: rgba(24, 24, 24, 0.13);
    border: 1px solid #bbb;
    color: #fff;
  }

  .result {
    margin-top: 10px;
    font-weight: 600;
    font-size: 0.8em;
    display: none;
    transition: display 0.4s ease;
  }

  .result.success {
    color: rgb(120, 192, 120);
  }

  .result.error {
    color: var(--red);
  }

  .form input:checked + label {
    border-color: var(--red);
    color: var(--red);
    background: var(--primary);
  }

  .form input[value="correct"]:checked + label {
    border-color: var(--green);
    color: rgb(16, 184, 16);
    background: var(--primary);
  }

  .form:has(input[value="correct"]:checked) .result.success {
    display: flex;
  }

  .form:has(input:not([value="correct"]):checked) .result.error {
    display: flex;
  }
</style>