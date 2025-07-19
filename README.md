# yemen-site
<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>موقع الجنة - الذكاء الاصطناعي للإجابات النفسية والروحية</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Amiri&display=swap');

  body {
    margin: 0;
    font-family: 'Amiri', serif;
    background: linear-gradient(135deg, #d0f0e4, #b2d8d8);
    color: #073b3a;
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100vh;
  }

  header {
    background: #0a8a7d;
    width: 100%;
    padding: 20px 0;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    text-align: center;
    color: #fff;
    position: relative;
  }

  .logo {
    font-size: 2.5rem;
    font-weight: bold;
    font-family: 'Amiri', serif;
    letter-spacing: 4px;
  }

  .logo span {
    font-size: 1.2rem;
    display: block;
    margin-top: 5px;
    font-weight: normal;
  }

  main {
    flex: 1;
    padding: 30px 15px;
    max-width: 600px;
    width: 100%;
  }

  h1 {
    text-align: center;
    margin-bottom: 30px;
    font-weight: 700;
  }

  textarea {
    width: 100%;
    height: 120px;
    padding: 12px;
    border-radius: 8px;
    border: 2px solid #0a8a7d;
    resize: none;
    font-size: 1.1rem;
    font-family: 'Amiri', serif;
    box-shadow: 0 0 8px rgba(10, 138, 125, 0.3);
  }

  button {
    margin-top: 15px;
    width: 100%;
    padding: 14px;
    background-color: #0a8a7d;
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 1.2rem;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  button:hover {
    background-color: #076655;
  }

  .response {
    margin-top: 30px;
    background: #e1f0ed;
    padding: 20px;
    border-radius: 10px;
    min-height: 100px;
    font-size: 1.1rem;
    line-height: 1.5;
    box-shadow: 0 0 15px rgba(0, 128, 110, 0.1);
    white-space: pre-wrap;
  }

  footer {
    text-align: center;
    padding: 15px 10px;
    font-size: 0.9rem;
    color: #0a8a7d;
  }
</style>
</head>
<body>

<header>
  <div class="logo">
    الجنة
    <span>محمد الحسني</span>
  </div>
</header>

<main>
  <h1>اسأل عن مشاعرك النفسية والروحية</h1>
  <textarea id="question" placeholder="اكتب سؤالك هنا..."></textarea>
  <button onclick="getAnswer()">اطلب الإجابة</button>

  <div class="response" id="answer"></div>
</main>

<footer>
  جميع الحقوق محفوظة &copy; 2025
</footer>

<script>
  function getAnswer() {
    const question = document.getElementById('question').value.trim();
    const answerDiv = document.getElementById('answer');

    if (!question) {
      answerDiv.textContent = 'الرجاء كتابة سؤال لنعطيك جوابًا.';
      return;
    }

    const responses = [
      "الصبر مفتاح الفرج، وثق بأن الله مع الصابرين.",
      "الراحة النفسية تبدأ باليقين والتوكل على الله.",
      "في كل أزمة حكمة، لا تفقد الأمل ولا تيأس.",
      "التفكر في نعم الله يزيل الهم ويهدئ النفس.",
      "الروح تحتاج إلى ذكر الله لتهدأ وتتوازن."
    ];

    const randomIndex = Math.floor(Math.random() * responses.length);
    const answer = responses[randomIndex];

    answerDiv.textContent = answer;
  }
</script>

</body>
</html>
