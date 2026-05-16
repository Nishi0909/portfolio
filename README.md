<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Nishi Patel Portfolio</title>

  <script src="https://cdn.tailwindcss.com"></script>

  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;700;800&display=swap" rel="stylesheet">

  <style>
    body {
      font-family: 'Plus Jakarta Sans', sans-serif;
      margin: 0;
      background: #f8fafc;
      color: #1e293b;
    }

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 40px;
      background: linear-gradient(135deg, #4f46e5, #ec4899);
      color: white;
    }

    .hero h1 {
      font-size: 70px;
      font-weight: 800;
      margin-bottom: 20px;
    }

    .hero p {
      font-size: 22px;
      max-width: 700px;
      margin: auto;
    }

    .btn {
      display: inline-block;
      margin-top: 30px;
      padding: 15px 30px;
      border-radius: 999px;
      background: white;
      color: #4f46e5;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }

    .btn:hover {
      transform: scale(1.05);
    }

    .section {
      padding: 80px 20px;
      max-width: 1200px;
      margin: auto;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
      gap: 30px;
      margin-top: 40px;
    }

    .card {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.08);
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-10px);
    }

    footer {
      padding: 50px;
      text-align: center;
      background: #111827;
      color: white;
    }
  </style>
</head>

<body>

  <section class="hero">
    <div>
      <h1>Nishi Patel</h1>

      <p>
        Business Analytics Graduate Student specializing in Data Analytics,
        Tableau, SQL, Python, and Strategic Decision Making.
      </p>

      <a class="btn" href="mailto:niship505@gmail.com">
        Contact Me
      </a>
    </div>
  </section>

  <section class="section">

    <h2 style="font-size:50px;font-weight:800;text-align:center;">
      Experience
    </h2>

    <div class="cards">

      <div class="card">
        <h3>Tata Consultancy Services</h3>

        <p>
          Quality Analytics Intern with experience in RPA automation,
          Tableau dashboards, and process optimization.
        </p>
      </div>

      <div class="card">
        <h3>Rhode Island State Government</h3>

        <p>
          Policy Research & Data Analytics Intern focusing on legislative
          data analysis and executive reporting.
        </p>
      </div>

      <div class="card">
        <h3>Projects</h3>

        <p>
          Nike Forecasting, Sephora Churn Analysis,
          IoT Smart Energy Analytics.
        </p>
      </div>

    </div>

  </section>

  <footer>
    <h2>Nishi Dineshkumar Patel</h2>

    <p>
      Columbia, Tennessee • Open to Opportunities
    </p>
  </footer>

</body>

</html>
