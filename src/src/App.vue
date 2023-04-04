<template>
  <WellcomePage @userdata="userData" v-if="pages.wellcomePage" :pages="pages"></WellcomePage>
  <div v-if="pages.quizePage">*Quize placeholder. Name - {{firstName}}</div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@600&display=swap');
*{
  margin: 0;
  padding: 0;
  font-family: Inter;
}
#app{
  overflow: hidden;
}
</style>

<script>
import WellcomePage from './components/WellcomePage.vue';

export default {
  components:{
    WellcomePage,
  },
  methods:{
    setLocalQuestions(){

    },
    userData(data){
      if (data.userFirstName) {
        this.firstName = data.userFirstName;
        this.pages.wellcomePage = false;
        this.pages.quizePage = true;
      }
    }
  },
  data(){
    return{
      pages: {wellcomePage: true, quizePage: false, resultPage: false},
      localQuestions: [],
      firstName: null,
      globalQuestions: [
          {
            question: "Question 1",
            answers: ["Answer1", "Answer2", "Answer3", "Answer4"],
            rightAnswerIndex: 0,
            userAnswerIndex: null,
            ifRight: "You are right",
            ifWrong: "You are wrong"
          },
          {
            question: "Question 2",
            answers: ["Answer1", "Answer2", "Answer3", "Answer4"],
            rightAnswerIndex: 0,
            userAnswerIndex: null,
            ifRight: "You are right",
            ifWrong: "You are wrong"
          },
          {
            question: "Question 3",
            answers: ["Answer1", "Answer2", "Answer3", "Answer4"],
            rightAnswerIndex: 0,
            userAnswerIndex: null,
            ifRight: "You are right",
            ifWrong: "You are wrong"
          },
          {
            question: "Question 4",
            answers: ["Answer1", "Answer2", "Answer3", "Answer4"],
            rightAnswerIndex: 0,
            userAnswerIndex: null,
            ifRight: "You are right",
            ifWrong: "You are wrong"
          },
          {
            question: "Question 5",
            answers: ["Answer1", "Answer2", "Answer3", "Answer4"],
            rightAnswerIndex: 0,
            userAnswerIndex: null,
            ifRight: "You are right",
            ifWrong: "You are wrong"
          },
          {
            question: "Question 6",
            answers: ["Answer1", "Answer2", "Answer3", "Answer4"],
            rightAnswerIndex: 0,
            userAnswerIndex: null,
            ifRight: "You are right",
            ifWrong: "You are wrong"
          },
          {
            question: "Question 7",
            answers: ["Answer1", "Answer2", "Answer3", "Answer4"],
            rightAnswerIndex: 0,
            userAnswerIndex: null,
            ifRight: "You are right",
            ifWrong: "You are wrong"
          },
          {
            question: "Question 8",
            answers: ["Answer1", "Answer2", "Answer3", "Answer4"],
            rightAnswerIndex: 0,
            userAnswerIndex: null,
            ifRight: "You are right",
            ifWrong: "You are wrong"
          },
          {
            question: "Question 9",
            answers: ["Answer1", "Answer2", "Answer3", "Answer4"],
            rightAnswerIndex: 0,
            userAnswerIndex: null,
            ifRight: "You are right",
            ifWrong: "You are wrong"
          },
          {
            question: "Question 10",
            answers: ["Answer1", "Answer2", "Answer3", "Answer4"],
            rightAnswerIndex: 0,
            userAnswerIndex: null,
            ifRight: "You are right",
            ifWrong: "You are wrong"
          },
        ]
    };
  }
}
</script>