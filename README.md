# index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Online Quiz</title>
    <link rel = "icon" href="idea.png">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <main class = "main">
        <header class = "header">
            <a href = "#" class = "logo">Quiz</a>
            <nav class = "navbar">
                <a href ="#" class="active">Home</a>
                <a href ="#">About</a>
                <a href ="#">Services</a>
                <a href ="#">Contact us</a>
            </nav>
        </header>
        <div class="container">
            <section class="quiz-section">
                <div class="quiz-box">
                    <h1> Quizzy Quiz</h1>
                    <div class="quiz-header">
                        <span>Quiz Website Tutorials</span>
                        <span class="header-score">Score: 0 / 5</span>
                    </div>
                    <h2 class="question-text">What does html stands for?</h2>
                    <div class="option-list"></div>
                    <div class="quiz-footer">
                        <span class="question-total">1 of 5 Questions</span>
                        <button class="next-btn">Next</button>
                    </div>
                </div>
                <div class="result-box">
                    <h2>Quiz result!</h2>
                    <div class="percentage-container">
                        <div class="circular-progress">
                            <span class="progress-value">0%</span>
                        </div>
                        <span class="score-text">Your Score 0 out of 5</span>
                    </div>
                    <div class="buttons">
                        <button class="tryAgain-btn">Try Again</button>
                        <button class="goHome-btn">Go TO Home</button>
                    </div>
                </div>
            </section>
            <section class="home">
                <div class="home-content">
                    <h1>Quiz Website</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eaque maiores explicabo unde reprehenderit? Consequatur sequi inventore vel, quasi id pariatur?</p>
                    <button class="start-btn">Start Quiz</button>
                </div>
            </section>
        </div>
    </main>
    <div class="popop-info">
        <h2>Quiz Guide</h2>
        <span class="info">Welcome to the Ultimate Full Stack Quiz Challenge! 🚀
            Test your coding knowledge with fun, fast-paced questions. Select the best answer, earn points, and climb the leaderboard. 💡 Sharpen your skills, learn new tech terms, and enjoy the game!</span>
        <div class="btn-group">
            <button class="info-btn exit-btn">Exit Quiz</button>
            <a href="#" class="info-btn continue-btn">Continue</a>
        </div>
    </div>
    <script src="script.js"></script>
    <script src="question.js"></script>
</body>
</html>


#style.css
* {
    margin:0;
    padding:0;
    box-sizing: border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body {
    color: white;
    background: black;
    overflow: hidden;
}

.header{
    position:fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 20px 10%;
    background: transparent;
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 100;
}

.logo{
    font-size: 32px;
    color: white;
    text-decoration: none;
    font-weight: 700;
    filter: drop-shadow(0 0 5px black)
}

.navbar a {
    font-size: 18px;
    color: white;
    text-decoration: none;
    font-weight: 500;
    margin-left: 35px;
    transition: .3s;
}
.navbar a:hover,
.navbar a.active{
    color: palevioletred;
}

.main{
    min-height: 100vh;
    background-image: url(quiz\ img.avif);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    pointer-events: auto;
    transition: .3s ease;
}

.main.active{
    filter: blur(15px);
    pointer-events: none;
}

.container{
    display: flex;
    height: 100vh;
    width: 200%;
}

.home{
    position: relative;
    left: -50%;
    min-height: 100vh;
    width:100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.home-content{
    max-width: 600px;
    display: flex;
    align-items: center;
    flex-direction: column;
}

.home-content h1{
    font-size: 78px;
    font-weight: 700;
    text-shadow: 0 0 10px rgba(0, 0, 0, .3);
}

.home-content p {
    font-size: 16px;
    text-align: center;
    text-shadow: 0 0 10px rgba(0, 0, 0, .3);
    margin-bottom: 30px;
}

.home-content .start-btn{
    width: 190px;
    height: 55px;
    background: palevioletred;
    border: 2px solid white;
    outline: none;
    border-radius: 6px;
    box-shadow: 0 0 10px plum;
    font-size: 18px;
    color: white;
    letter-spacing: 1px;
    font-weight: 600;
    cursor: pointer;
    transition: .5s;
}

.home-content .start-btn:hover{
    background: black;
    box-shadow: none;
}

.popop-info{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(.9);
    width: 500px;
    background: white;
    border-radius: 6px;
    padding: 10px 25px;
    opacity: 0;
    pointer-events: none;
    transition: .3s ease;
}

.popop-info.active{
    opacity: 1;
    pointer-events: auto;
    transform: translate(-50%, -50%) scale(1);
}

.popop-info h2{
    font-size: 50px;
    color: palevioletred;
}

.popop-info .info{
    display: inline-block;
    font-size: 16px;
    color: black;
    font-weight: 500;
    margin: 4px 0 ;
}

.popop-info .btn-group{
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 1px solid black;
    margin-top: 10px;
    padding: 15px 0 7px;
}

.popop-info .btn-group .info-btn{
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 130px;
    height: 45px;
    background: plum;
    border: 2px solid plum;
    outline: none;
    border-radius:6px ;
    text-decoration: none;
    font-size: 16px;
    color: white;
    font-weight: 600;
    box-shadow: 0 0 10px rgba(0, 0, 0, .1);
    cursor: pointer;
    transition: .5s;
}

.popop-info .btn-group .info-btn:nth-child(1){
    background: transparent;
    color: palevioletred;
}

.popop-info .btn-group .info-btn:nth-child(1):hover{
    background: palevioletred;
    color: white;
}

.popop-info .btn-group .info-btn:nth-child(2):hover{
    background: palevioletred;
    border-color: palevioletred;
}

.quiz-section{
    position: relative;
    left: -50%;
    width: 100%;
    background: black;
    z-index: 100;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: .8s ease-in-out;
    transition-delay: .25s;
}

.quiz-section.active{
    left:0;
}

.quiz-section .quiz-box{
    position: relative;
    width: 500px;
    background: transparent;
    border: 2px solid plum;
    border-radius: 6px;
    display: flex;
    flex-direction: column;
    padding: 20px 30px;
    opacity: 0;
    pointer-events: none;
    transform: scale(.9);
    transition: .3s ease;
    transition-delay: 0s;
}

.quiz-section .quiz-box.active{
    opacity: 1;
    pointer-events: auto;
    transform: scale(1);
    transition: 1s ease;
    transition-delay: 1s;
}


.quiz-box h1{
    font-size: 32px;
    text-align: center;
    background: linear-gradient(45deg, transparent, palevioletred, transparent);
    border-radius: 6px;
}

.quiz-box .quiz-header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 0;
    border-bottom: 2px solid plum;
    margin-bottom: 30px;
}
.quiz-header span{
    font-size: 18px;
    font-weight: 500;
}

.quiz-header .header-score{
    background: palevioletred;
    border-radius: 3px;
    padding: 7px;
}

.quiz-box .question-text{
    font-size: 24px;
    font-weight: 600;
}

.option-list .option{
    width: 100%;
    padding: 12px;
    background: transparent;
    border: 2px solid rgba(255, 255, 255, .2);
    border-radius: 4px;
    font-size: 17px;
    margin: 15px 0;
    cursor: pointer;
    transition: .3s;
}

.option-list .option:hover{
    background: rgba(255, 255, 255, .1);
    border-color: rgba(255, 255, 255, .1);
}


.option-list .option.correct{
    background: black;
    color: seagreen;
    border-color: seagreen;
}

.option-list .option.incorrect{
    background: black;
    color: red;
    border-color: red;
}

.option-list .option.disabled{
    pointer-events: none;
}


.quiz-box .quiz-footer{
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 2px solid plum;
    padding-top: 20px;
    margin-top: 25px;
}

.quiz-footer .question-total{
    font-size: 16px;
    font-weight: 600;
}

.quiz-footer .next-btn{
    width: 100px;
    height: 45px;
    background: rgba(255, 255, 255, .1);
    border: 2px solid rgba(255, 255, 255, .1);
    outline: none;
    border-radius: 6px;
    font-size: 16px;
    color: rgba(255, 255, 255, .3);
    font-weight: 600;
    cursor: pointer;
    pointer-events: none;
    transition: .5s;
}

.quiz-footer .next-btn.active{
    pointer-events: auto;
    background: plum;
    border-color: plum;
    color: white;
}

.quiz-footer .next-btn.active:hover{
    background: palevioletred;
    border-color: plum;
}

.quiz-section .result-box{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(.9);
    width: 500px;
    background: transparent;
    border: 2px solid palevioletred;
    border-radius: 6px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    opacity: 0;
    pointer-events: none;
    transition: .3s ease;
}

.quiz-section .result-box.active{
    opacity: 1;
    pointer-events: auto;
    transform: translate(-50%, -50%) scale(1);
}

.result-box h2{
    font-size: 52px;
}

.result-box .percentage-container{
    width: 300px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 20px 0 40px;
}

.percentage-container .circular-progress{
    position: relative;
    width: 250px;
    height: 250px;
    background: conic-gradient(purple 3.6deg, rgba(255, 255, 255, .1) 0deg);
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.percentage-container .circular-progress::before{
    content: '';
    position: absolute;
    width: 210px;
    height: 210px;
    background: black;
    border-radius: 50%;
}

.circular-progress .progress-value{
    position: relative;
    font-size: 45px;
    font-weight: 600;
}

.percentage-container .score-text{
    font-size: 26px;
    font-weight: 600;
    margin-top: 20px;
}

.result-box .buttons{
    display: flex;
}

.buttons button{
    width: 130px;
    height: 47px;
    background: palevioletred;
    border: 2px solid palevioletred;
    outline: none;
    border-radius: 6px;
    font-size: 16px;
    color: white;
    font-weight: 600;
    margin: 0 20px 20px;
    cursor: pointer;
    transition: .5s;
}

.buttons button:nth-child(1):hover{
    background: palevioletred;
    border-color: plum;
}

.buttons button:nth-child(2){
    background: transparent;
    color: palevioletred;
}

.buttons button:nth-child(2):hover{
    background: palevioletred;
    color: white;
}


#script.js
const startBtn = document.querySelector('.start-btn');
const popopInfo = document.querySelector('.popop-info');
const exitBtn = document.querySelector('.exit-btn');
const main = document.querySelector('.main');
const continueBtn = document.querySelector('.continue-btn');
const quizSection = document.querySelector('.quiz-section');
const quizBox = document.querySelector('.quiz-box');
const resultBox = document.querySelector('.result-box');
const tryAgainBtn = document.querySelector('.tryAgain-btn');
const goHomeBtn = document.querySelector('.goHome-btn');

startBtn.onclick = () => {
    popopInfo.classList.add('active');
    main.classList.add('active');
}

exitBtn.onclick = () => {
    popopInfo.classList.remove('active');
    main.classList.remove('active');
}

continueBtn.onclick = () => {
    quizSection.classList.add('active');
    popopInfo.classList.remove('active');
    main.classList.remove('active');
    quizBox.classList.add('active');

    showQuestions(0);
    questionCounter(1);
    headerScore();
}

tryAgainBtn.onclick = () => {
    quizBox.classList.add('active');
    nextBtn.classList.remove('active');
    resultBox.classList.remove('active');

    questionCount = 0;
    questionNum = 1;
    userScore = 0;
    showQuestions(questionCount);
    questionCounter(questionNum);

    headerScore();
}

goHomeBtn.onclick = () => {
    quizSection.classList.remove('active');
    nextBtn.classList.remove('active');
    resultBox.classList.remove('active');

    questionCount = 0;
    questionNum = 1;
    userScore = 0;
    showQuestions(questionCount);
    questionCounter(questionNum);

    headerScore();
}

let questionCount = 0;
let questionNum = 1;
let userScore = 0;

const nextBtn = document.querySelector('.next-btn');
const optionList = document.querySelector('.option-list');

nextBtn.onclick = () => {
    if(questionCount < questions.length - 1){
        questionCount++;
        showQuestions(questionCount);

        questionNum++;
        questionCounter(questionNum);

        nextBtn.classList.remove('active');
    }
    else{
        showResultBox();
    }
}

function showQuestions(index){
    const questionText = document.querySelector('.question-text');
    questionText.textContent = `${questions[index].num}. ${questions[index].questions}`;

    let optionTag = `<div class="option"><span>${questions[index].options[0]}</span></div>
                     <div class="option"><span>${questions[index].options[1]}</span></div>
                     <div class="option"><span>${questions[index].options[2]}</span></div>
                     <div class="option"><span>${questions[index].options[3]}</span></div>`;

    optionList.innerHTML = optionTag;

    const option = document.querySelectorAll('.option');
    for (let i = 0; i < option.length; i++){
        option[i].setAttribute('onclick', 'optionSelected(this)');
    }
}

function optionSelected(answer){
    let userAnswer = answer.textContent;
    let correctAnswer = questions[questionCount].answer;
    let allOptions = optionList.children.length;

    if (userAnswer == correctAnswer){
        answer.classList.add('correct');
        userScore += 1;
        headerScore();
    }
    else{
        answer.classList.add('incorrect');

        for(let i = 0; i < allOptions; i++){
            if (optionList.children[i].textContent == correctAnswer){
                optionList.children[i].setAttribute('class', 'option correct');
            }
        }
    }

    for(let i = 0; i < allOptions; i++){
        optionList.children[i].classList.add('disabled');
    }

    nextBtn.classList.add('active');
}

function questionCounter(index){
    const questionTotal = document.querySelector('.question-total');
    questionTotal.textContent = `${index} of ${questions.length} Questions`;
}

function headerScore(){
    const headerScoreText = document.querySelector('.header-score');
    headerScoreText.textContent = `Score: ${userScore} / ${questions.length}`;
}

function showResultBox(){
    quizBox.classList.remove('active');
    resultBox.classList.add('active');

    const scoreText = document.querySelector('.score-text');
    scoreText.textContent = `Your Score ${userScore} out of ${questions.length}`;

    const circularProgress = document.querySelector('.circular-progress');
    const progressValue = document.querySelector('.progress-value');
    let progressStartValue = -1;
    let progressEndValue = (userScore / questions.length) * 100;
    let speed = 20;

    let progress = setInterval(() => {
        progressStartValue++;
        progressValue.textContent = `${progressStartValue}%`;
        circularProgress.style.background = `conic-gradient(purple ${progressStartValue * 3.6}deg, rgba(255, 255, 255, .1) 0deg)`;

        if (progressStartValue == progressEndValue){
            clearInterval(progress);
        }
    }, speed);
}


#question.js
let questions = [
    {
        num: 1,
        questions: "What does html stands for?",
        answer: "C) Hyper Text Markup Language",
        options: [
            "A) Hyper Type Multi Language",
            "B) Hyper Text Multiple Language",
            "C) Hyper Text Markup Language",
            "D) Home Text Multi Language"
        ]
    },
    {
        num: 2,
        questions: "What language is used for styling web pages?",
        answer: "B) CSS ",
        options: [
            "A) HTML",
            "B) CSS ",
            "C) JavaScript",
            "D) SQL"
        ]
    },
    {
        num: 3,
        questions: "What does SQL stand for?",
        answer: "B) Structured Query Language",
        options: [
            "A) Simple Query Language",
            "B) Structured Query Language",
            "C) Standard Question Language",
            "D) Server Query Language"
        ]
    },
    {
        num: 4,
        questions: "Which of these is a NoSQL database?",
        answer: "C) MongoDB",
        options: [
            "A) MySQL",
            "B) PostgreSQL",
            "C) MongoDB",
            "D) Oracle"
        ]
    },
    {
        num: 5,
        questions: "What is the main function of the backend in web development?",
        answer: "C) Manage database and server logic",
        options: [
            "A) Design layouts",
            "B) Handle user input",
            "C) Manage database and server logic",
            "D) Create animations"
        ]
    }
];
