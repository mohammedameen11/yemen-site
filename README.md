 <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>نور الأمل</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Cairo&display=swap');

  body {
    margin: 0;
    font-family: 'Cairo', sans-serif;
    background: linear-gradient(135deg, #ccefff, #e0f7fa);
    color: #333;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  header {
    background-color: #0288d1;
    color: white;
    padding: 20px;
    text-align: center;
    box-shadow: 0 2px 8px rgba(0,0,0,0.2);
  }

  header h1 {
    margin: 0;
    font-weight: 700;
  }

  main {
    flex: 1;
    max-width: 700px;
    margin: 40px auto;
    padding: 0 20px;
  }

  section.intro {
    text-align: center;
    margin-bottom: 40px;
  }

  section.intro h2 {
    font-weight: 600;
    font-size: 1.8rem;
  }

  section.intro p {
    font-size: 1.2rem;
    color: #555;
    margin-top: 10px;
  }

  section.contact {
    background: white;
    padding: 25px;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
  }

  section.contact h3 {
    margin-top: 0;
    margin-bottom: 15px;
    color: #0288d1;
  }

  label {
    display: block;
    margin-bottom: 6px;
    font-weight: 600;
  }

  input, textarea {
    width: 100%;
    padding: 10px;
    border: 2px solid #0288d1;
    border-radius: 6px;
    margin-bottom: 15px;
    font-size: 1rem;
    font-family: 'Cairo', sans-serif;
  }

  textarea {
    resize: vertical;
    min-height: 80px;
  }

  button {
    background-color: #0288d1;
    color: white;
    border: none;
    padding: 12px 20px;
    font-size: 1.1rem;
    border-radius: 8px;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  button:hover {
    background-color: #026aa7;
  }

  footer {
    text-align: center;
    padding: 15px 10px;
    font-size: 0.9rem;
    color: #555;
    background: #e0f7fa;
  }
</style>
</head>
<body>

<header>
  <h1>نور الأمل</h1>
</header>

<main>
  <section class="intro">
    <h2>مرحباً بك في موقع نور الأمل</h2>
    <p>مساحتك الصغيرة للاسترخاء، التفاؤل، ومشاركة الأفكار الجميلة.</p>
  </section>

  <section class="contact">
    <h3>تواصل معنا</h3>
    <form id="contactForm">
      <label for="name">الاسم</label>
      <input type="text" id="name" placeholder="اكتب اسمك" required />

      <label for="email">البريد الإلكتروني</label>
      <input type="email" id="email" placeholder="اكتب بريدك الإلكتروني" required />

      <label for="message">رسالتك</label>
      <textarea id="message" placeholder="اكتب رسالتك هنا..." required></textarea>

      <button type="submit">أرسل</button>
    </form>
    <p id="responseMsg" style="color:green; display:none; margin-top: 10px;">شكرًا لتواصلك معنا!</p>
  </section>
</main>

<footer>
  &copy; 2025 نور الأمل. جميع الحقوق محفوظة.
</footer>

<script>
  const form = document.getElementById('contactForm');
  const responseMsg = document.getElementById('responseMsg');

  form.addEventListener('submit', (e) => {
    e.preventDefault();
    responseMsg.style.display = 'block';
    form.reset();
  });
</script>

</body>
</html>
