# Abu-oken
IELTS Band 9 Interactive Learning Platform (A1–C2) with vocabulary, grammar and academic reading system
Your site is live at https://khudoyberdiyevabdurazzoq-dotcom.github.io/Xudoyberdiyev abdurazzoq
<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>IELTS Band 9 Platform | Abdurazzoq</title>

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:Arial;}

body{
  background:#070b17;
  color:white;
}

/* HEADER */
header{
  text-align:center;
  padding:40px;
  background:linear-gradient(135deg,#0f172a,#1e293b);
}

header h1{
  color:#38bdf8;
  font-size:40px;
}

header p{
  color:#cbd5e1;
  margin-top:10px;
}

/* GRID */
.container{
  padding:50px 10%;
}

.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:20px;
}

.card{
  background:#111827;
  padding:25px;
  border-radius:16px;
  cursor:pointer;
  transition:0.3s;
  border:1px solid #1f2937;
}

.card:hover{
  transform:translateY(-10px);
  box-shadow:0 0 20px #38bdf8;
}

.card h2{
  color:#38bdf8;
}

/* MODAL */
.modal{
  display:none;
  position:fixed;
  top:0;left:0;
  width:100%;height:100%;
  background:rgba(0,0,0,0.85);
  justify-content:center;
  align-items:center;
}

.box{
  background:#0f172a;
  width:90%;
  max-width:800px;
  padding:25px;
  border-radius:20px;
  max-height:90vh;
  overflow:auto;
}

.close{
  float:right;
  cursor:pointer;
  color:red;
  font-size:22px;
}

.item{
  background:#111827;
  padding:12px;
  margin:10px 0;
  border-radius:10px;
}

/* ARTICLE */
.article{
  background:#0b1220;
  padding:15px;
  border-radius:12px;
  border-left:3px solid #38bdf8;
  margin-top:10px;
  line-height:1.6;
}

.word{
  color:#38bdf8;
  font-weight:bold;
}
</style>
</head>

<body>

<header>
  <h1>IELTS Band 9 Learning Platform</h1>
  <p>A1 → C2 | Vocabulary + Grammar + Articles + IELTS Strategy</p>
</header>

<div class="container">

<div class="grid">

  <div class="card" onclick="openLevel('A1')"><h2>A1</h2><p>Beginner</p></div>
  <div class="card" onclick="openLevel('A2')"><h2>A2</h2><p>Elementary</p></div>
  <div class="card" onclick="openLevel('B1')"><h2>B1</h2><p>Intermediate</p></div>
  <div class="card" onclick="openLevel('B2')"><h2>B2</h2><p>Upper Intermediate</p></div>
  <div class="card" onclick="openLevel('C1')"><h2>C1</h2><p>Advanced</p></div>
  <div class="card" onclick="openLevel('C2')"><h2>C2</h2><p>Mastery</p></div>

</div>

</div>

<!-- MODAL -->
<div class="modal" id="modal">
  <div class="box">

    <span class="close" onclick="closeModal()">✖</span>
    <h2 id="title"></h2>
    <div id="content"></div>

  </div>
</div>

<script>

const data = {

A1:{
vocab:[
{w:"Book",t:"kitob",e:"I read a book."},
{w:"Eat",t:"yemoq",e:"I eat food."}
],
grammar:"To be (am/is/are), simple sentences",
article:"Learning English starts with small steps. First, learn basic words like book, eat, house. Practice every day for 10 minutes."
},

A2:{
vocab:[
{w:"Important",t:"muhim",e:"English is important."},
{w:"Travel",t:"safar",e:"I travel often."}
],
grammar:"Past Simple introduction",
article:"At A2 level, you should start speaking in past tense. Try to describe your daily life and past activities."
},

B1:{
vocab:[
{w:"Improve",t:"yaxshilash",e:"I improve my skills."},
{w:"Experience",t:"tajriba",e:"Work experience is useful."}
],
grammar:"Past Continuous + Future forms",
article:"B1 learners should focus on speaking fluently. Try thinking in English instead of translating."
},

B2:{
vocab:[
{w:"Achieve",t:"erishmoq",e:"I achieved my goal."},
{w:"Develop",t:"rivojlantirmoq",e:"Develop your skills."}
],
grammar:"Passive voice + conditionals",
article:"At B2 level, you must start using complex sentences and academic vocabulary."
},

C1:{
vocab:[
{w:"Sophisticated",t:"murakkab",e:"Sophisticated idea"},
{w:"Comprehensive",t:"to‘liq",e:"Comprehensive analysis"}
],
grammar:"Advanced grammar + inversion",
article:"C1 learners must write essays and use advanced grammar structures like inversion and nominalisation."
},

C2:{
vocab:[
{w:"Unprecedented",t:"misli ko‘rilmagan",e:"Unprecedented change"},
{w:"Meticulous",t:"juda ehtiyotkor",e:"Meticulous work"}
],
grammar:"Native-like fluency, idioms, academic mastery",
article:"C2 is native-level English. You must think, speak, and write like an academic expert."
}

};

function openLevel(lvl){

document.getElementById("modal").style.display="flex";
document.getElementById("title").innerText = lvl + " Level";

let html = "<h3>Vocabulary</h3>";

data[lvl].vocab.forEach(v=>{
html += `
<div class='item'>
<div class='word'>${v.w} - ${v.t}</div>
<div>${v.e}</div>
</div>`;
});

html += "<h3>Grammar</h3>";
html += "<div class='item'>" + data[lvl].grammar + "</div>";

html += "<h3>Article</h3>";
html += "<div class='article'>" + data[lvl].article + "</div>";

document.getElementById("content").innerHTML = html;

}

function closeModal(){
document.getElementById("modal").style.display="none";
}

</script>

</body>
</html>
