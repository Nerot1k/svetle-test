   <div class="quiz-container" id="quiz">

        <div class="quiz-header">
            <h1 id="title">МузВикторина <img class="photo svelte-192ixv5" src="/img/f1.jpg" alt="photo" width="200"></h1>
            <h2 id="question">Вопрос1</h2>
            <ul>
                <li>
                    <input type="radio" name="answer" id="a" class="answer">
                    <label for="a" id="a_text">*</label>
                </li>

                <li>
                    <input type="radio" name="answer" id="b" class="answer">
                    <label for="b" id="b_text">*</label>
                </li>

                <li>
                    <input type="radio" name="answer" id="c" class="answer">
                    <label for="c" id="c_text">*</label>
                </li>

                <li>
                    <input type="radio" name="answer" id="d" class="answer">
                    <label for="d" id="d_text">*</label>
                </li>

            </ul>
        </div>

        <button id="submit">Следующий вопрос</button>

    </div>

<script>

const quizData = [
    {
        question: "Какой из предложенных вариантов не является струнно-щепковым музыкальным инструментом?",
        a: "Барабан",
        b: "Укулеле",
        c: "Арфа",
        d: "Электрогитара",
        correct: "a"
 },
    {
        question: "Чем отличается Акустическая гитара от Классической?",
        a: "Барабан, то есть корпус самой гитары",
        b: "Гриф",
        c: "Форма колков и то, как они выглядят",
        d: "Длиной струн",
        correct: "c"
    }, {
        question: "Кто из этих исполнителей прославился игрой на электрогитаре?",
        a: "Высоцкий",
        b: "В. Цой",
        c: "Пол Маккартни",
        d: "Курт Кобейн",
        correct: "d",
    }, {
        question: "Что такое мензура в гитаре?",
        a: "Длина струн",
        b: "Расстояние от верхнего до нижнего порожка",
        c: "То, за что крепятся струны",
        d: "Приём, для смены звука",
        correct: "b"
    }, {
        question: "Из каких материалов не сущесвтует Медиаторов?",
        a: "Из кости",
        b: "Из глянца",
        c: "Из пластика",
        d: "Из дерева",
        correct: "b",
    }
]
const quiz = document.getElementById('quiz')
const answerEls = document.querySelectorAll('.answer')
const questionEl = document.getElementById('question')
const a_text = document.getElementById('a_text')
const b_text = document.getElementById('b_text')
const c_text = document.getElementById('c_text')
const d_text = document.getElementById('d_text')
const submitBtn = document.getElementById('submit')


let currentQuiz = 0
let score = 0

loadQuiz()

function loadQuiz() {

    deselectAnswers()

    const currentQuizData = quizData[currentQuiz]

    questionEl.innerText = currentQuizData.question
    a_text.innerText = currentQuizData.a
    b_text.innerText = currentQuizData.b
    c_text.innerText = currentQuizData.c
    d_text.innerText = currentQuizData.d
}

function deselectAnswers() {
    answerEls.forEach(answerEl => answerEl.checked = false)
}

function getSelected() {
    let answer
    answerEls.forEach(answerEl => {
        if (answerEl.checked) {
            answer = answerEl.id
        }
    })
    return answer
}


submitBtn.addEventListener('click', () => {
    const answer = getSelected()
    if (answer) {
        if (answer === quizData[currentQuiz].correct) {
            score++
        }

        currentQuiz++

        if (currentQuiz < quizData.length) {
            loadQuiz()
        } else {
            quiz.innerHTML = `
           <h2>Вы ответили верно на    ${score}  из  ${quizData.length} заданных вопросов</h2>

           <button onclick="location.reload()">Пройти заново</button>
           `
        }
    }
})


</script>

    <style>
        
        * {
    box-sizing: border-box;
}

body {
    background-color: #b8c6db;
    background-image: linear-gradient(315deg, #b8c6db 0%, #f5f7f7 100%);
    font-family: 'Poppins', sans-serif;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    overflow: hidden;
    margin: 0;
}

.quiz-container {
    background-color: #F1F1F1;
    border-radius: 10px;
    box-shadow: 0 0 10px 2px rgba(100, 100, 100, 0.1);
    width: 500px;
    overflow: hidden;
}

.quiz-header {
    padding: 40px;
}

h1 {
    padding: 10px;
    text-align: center;
    margin: 0;
    color: #4682B4;
    padding: 60px;
}

h2 {
    padding: 1rem;
    text-align: center;
    margin: 0;

}

ul {
    list-style-type: none;
    padding: 0;
}

ul li {
    font-size: 18px;
    margin: 10px 0;
}

ul li label {
    cursor: pointer;
}

button {
    background-color: #76C835;
    color: #fff;
    border: none;
    display: block;
    width: 100%;
    cursor: pointer;
    font-size: 21px;
    font-family: inherit;
    padding: 23px;
}

button:hover {
    background-color: #039E50;
}

button:focus {
    outline: none;
    background-color: #03654D;
}

        </style>