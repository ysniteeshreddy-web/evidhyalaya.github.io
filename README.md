# evidhyalaya.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>E Vidhyalaya</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body { font-family: 'Segoe UI', sans-serif; color: #2c2c2a; background: #fff; }

  /* NAV */
  nav { background: #fff; border-bottom: 1px solid #e0ddd5; padding: 0 5%; display: flex; justify-content: space-between; align-items: center; height: 64px; position: sticky; top: 0; z-index: 100; }
  .logo { display: flex; align-items: center; gap: 10px; }
  .logo-icon { width: 36px; height: 36px; background: #faeedb; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 18px; }
  .logo-text { font-size: 17px; font-weight: 600; color: #2c2c2a; }
  .nav-links { display: flex; gap: 28px; list-style: none; }
  .nav-links a { text-decoration: none; color: #5f5e5a; font-size: 14px; transition: color .2s; }
  .nav-links a:hover { color: #ba7517; }

  /* HERO */
  .hero { background: linear-gradient(135deg, #faeeda 0%, #e1f5ee 100%); padding: 80px 5% 90px; display: flex; align-items: center; justify-content: space-between; gap: 40px; }
  .hero-text { max-width: 540px; }
  .hero-tag { display: inline-block; background: #faeedb; color: #854f0b; font-size: 12px; font-weight: 600; padding: 4px 12px; border-radius: 20px; margin-bottom: 16px; letter-spacing: .5px; text-transform: uppercase; }
  .hero h1 { font-size: 42px; font-weight: 700; color: #2c2c2a; line-height: 1.2; margin-bottom: 16px; }
  .hero h1 span { color: #ba7517; }
  .hero p { font-size: 17px; color: #5f5e5a; line-height: 1.7; margin-bottom: 28px; }
  .btn { display: inline-block; background: #ba7517; color: #fff; padding: 12px 28px; border-radius: 8px; font-size: 15px; font-weight: 600; text-decoration: none; transition: background .2s; cursor: pointer; border: none; }
  .btn:hover { background: #854f0b; }
  .btn-outline { background: transparent; color: #ba7517; border: 2px solid #ba7517; margin-left: 12px; }
  .btn-outline:hover { background: #faeeda; }
  .hero-illustration { font-size: 120px; user-select: none; flex-shrink: 0; }

  /* STATS BAR */
  .stats { background: #2c2c2a; padding: 28px 5%; display: flex; justify-content: space-around; flex-wrap: wrap; gap: 20px; }
  .stat { text-align: center; }
  .stat-num { font-size: 32px; font-weight: 700; color: #fac775; }
  .stat-label { font-size: 13px; color: #b4b2a9; margin-top: 2px; }

  /* SECTION */
  section { padding: 72px 5%; }
  .section-tag { display: inline-block; font-size: 12px; font-weight: 600; padding: 4px 12px; border-radius: 20px; letter-spacing: .5px; text-transform: uppercase; margin-bottom: 10px; }
  .tag-amber { background: #faeeda; color: #854f0b; }
  .tag-teal { background: #e1f5ee; color: #0f6e56; }
  h2.section-title { font-size: 32px; font-weight: 700; color: #2c2c2a; margin-bottom: 10px; }
  .section-sub { font-size: 16px; color: #5f5e5a; max-width: 560px; line-height: 1.7; margin-bottom: 40px; }

  /* ADMISSIONS */
  .admissions { background: #fff; }
  .steps { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; }
  .step-card { background: #fafaf8; border: 0.5px solid #d3d1c7; border-radius: 12px; padding: 24px 20px; position: relative; }
  .step-num { width: 36px; height: 36px; background: #faeedb; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: 700; color: #854f0b; font-size: 16px; margin-bottom: 14px; }
  .step-card h3 { font-size: 15px; font-weight: 600; color: #2c2c2a; margin-bottom: 8px; }
  .step-card p { font-size: 13px; color: #5f5e5a; line-height: 1.6; }

  .info-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 16px; margin-top: 32px; }
  .info-pill { background: #e1f5ee; border-radius: 10px; padding: 16px 18px; }
  .info-pill .label { font-size: 11px; color: #0f6e56; font-weight: 600; text-transform: uppercase; letter-spacing: .5px; margin-bottom: 4px; }
  .info-pill .value { font-size: 15px; color: #085041; font-weight: 600; }

  /* ACADEMICS */
  .academics { background: #f9f8f5; }
  .courses-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 16px; }
  .course-card { background: #fff; border: 0.5px solid #d3d1c7; border-radius: 12px; padding: 22px 16px; text-align: center; transition: box-shadow .2s, transform .2s; cursor: default; }
  .course-card:hover { transform: translateY(-3px); box-shadow: 0 6px 20px rgba(0,0,0,.07); }
  .course-icon { font-size: 32px; margin-bottom: 10px; }
  .course-card h3 { font-size: 14px; font-weight: 600; color: #2c2c2a; margin-bottom: 6px; }
  .course-card p { font-size: 12px; color: #888780; line-height: 1.5; }

  /* FOOTER */
  footer { background: #2c2c2a; color: #b4b2a9; padding: 40px 5%; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 20px; }
  .footer-logo { font-size: 18px; font-weight: 700; color: #fac775; }
  .footer-contact { font-size: 13px; line-height: 1.8; }
  .footer-contact a { color: #9fe1cb; text-decoration: none; }
  .footer-bottom { width: 100%; text-align: center; font-size: 12px; border-top: 0.5px solid #444441; padding-top: 20px; margin-top: 10px; color: #888780; }

  @media (max-width: 640px) {
    .hero { flex-direction: column; text-align: center; }
    .hero-illustration { font-size: 80px; }
    .hero h1 { font-size: 30px; }
    .nav-links { display: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="logo">
    <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAgGBgcGBQgHBwcJCQgKDBQNDAsLDBkSEw8UHRofHh0aHBwgJC4nICIsIxwcKDcpLDAxNDQ0Hyc5PTgyPC4zNDL/2wBDAQkJCQwLDBgNDRgyIRwhMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjL/wAARCADIAMgDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD5/ooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigD/2Q==" alt="E Vidhyalaya Logo" style="height:40px; width:40px; border-radius:50%; object-fit:cover;">
    <span class="logo-text">E Vidhyalaya</span>
  </div>
  <ul class="nav-links">
    <li><a href="#admissions">Admissions</a></li>
    <li><a href="#academics">Academics</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-text">
    <span class="hero-tag">Welcome to E Vidhyalaya</span>
    <h1>Where Every Child <span>Grows</span> and Learns</h1>
    <p>A nurturing and joyful learning environment for children aged 4–11. We inspire curiosity, creativity, and a lifelong love of learning.</p>
    <a href="#admissions" class="btn">Apply Now</a>
    <a href="#academics" class="btn btn-outline">Our Curriculum</a>
  </div>
  <div class="hero-illustration">🏫</div>
</section>

<!-- STATS -->
<div class="stats">
  <div class="stat"><div class="stat-num">450+</div><div class="stat-label">Happy Students</div></div>
  <div class="stat"><div class="stat-num">32</div><div class="stat-label">Qualified Teachers</div></div>
  <div class="stat"><div class="stat-num">15+</div><div class="stat-label">Extracurriculars</div></div>
  <div class="stat"><div class="stat-num">25 yrs</div><div class="stat-label">Of Excellence</div></div>
</div>

<!-- ADMISSIONS -->
<section class="admissions" id="admissions">
  <span class="section-tag tag-amber">Admissions</span>
  <h2 class="section-title">Join Our School Family</h2>
  <p class="section-sub">Enrolling your child at Sunshine Primary is simple. Follow these steps to secure your child's place for the upcoming school year.</p>

  <div class="steps">
    <div class="step-card">
      <div class="step-num">1</div>
      <h3>Enquire Online</h3>
      <p>Fill in our enquiry form or call us to learn more about available places and our school community.</p>
    </div>
    <div class="step-card">
      <div class="step-num">2</div>
      <h3>School Visit</h3>
      <p>Attend an open day or schedule a personal tour to see our classrooms, playgrounds, and meet our staff.</p>
    </div>
    <div class="step-card">
      <div class="step-num">3</div>
      <h3>Submit Application</h3>
      <p>Complete the admission form and submit required documents including birth certificate and vaccination records.</p>
    </div>
    <div class="step-card">
      <div class="step-num">4</div>
      <h3>Confirmation</h3>
      <p>Receive your offer letter and complete enrollment formalities before the academic year begins.</p>
    </div>
  </div>

  <div class="info-grid">
    <div class="info-pill"><div class="label">Age Range</div><div class="value">4 – 11 years</div></div>
    <div class="info-pill"><div class="label">Enrollment Opens</div><div class="value">January 2026</div></div>
    <div class="info-pill"><div class="label">Academic Year</div><div class="value">June – April</div></div>
    <div class="info-pill"><div class="label">Class Size</div><div class="value">Max 25 students</div></div>
  </div>
</section>

<!-- ACADEMICS -->
<section class="academics" id="academics">
  <span class="section-tag tag-teal">Academics</span>
  <h2 class="section-title">A Balanced Curriculum</h2>
  <p class="section-sub">Our holistic program blends core academics with arts, sports, and life skills to develop well-rounded young learners.</p>

  <div class="courses-grid">
    <div class="course-card">
      <div class="course-icon">📖</div>
      <h3>English & Literacy</h3>
      <p>Reading, writing, grammar and storytelling for confident communicators.</p>
    </div>
    <div class="course-card">
      <div class="course-icon">🔢</div>
      <h3>Mathematics</h3>
      <p>Number sense, problem solving, and logical thinking from an early age.</p>
    </div>
    <div class="course-card">
      <div class="course-icon">🔬</div>
      <h3>Science</h3>
      <p>Hands-on experiments and exploration of the natural world.</p>
    </div>
    <div class="course-card">
      <div class="course-icon">🌍</div>
      <h3>Social Studies</h3>
      <p>History, geography, and civic values to build global citizens.</p>
    </div>
    <div class="course-card">
      <div class="course-icon">🎨</div>
      <h3>Arts & Crafts</h3>
      <p>Painting, drawing, and creative projects to spark imagination.</p>
    </div>
    <div class="course-card">
      <div class="course-icon">🎵</div>
      <h3>Music</h3>
      <p>Rhythm, instruments, and performance for young musicians.</p>
    </div>
    <div class="course-card">
      <div class="course-icon">⚽</div>
      <h3>Physical Education</h3>
      <p>Sports, movement, and teamwork for healthy, active children.</p>
    </div>
    <div class="course-card">
      <div class="course-icon">💻</div>
      <h3>Digital Literacy</h3>
      <p>Age-appropriate introduction to technology and digital skills.</p>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer id="contact">
  <div>
    <div class="footer-logo">E Vidhyalaya</div>
    <p style="font-size:13px; margin-top:6px; color:#888780;">Nurturing young minds every day</p>
  </div>
  <div class="footer-contact">
    <strong style="color:#d3d1c7;">Contact Us</strong><br>
    📍 123 Learning Lane, Hyderabad 500001<br>
    📞 <a href="tel:+914012345678">+91 40 1234 5678</a><br>
    ✉️ <a href="mailto:info@sunshineprimary.edu">info@sunshineprimary.edu</a>
  </div>
  <div class="footer-bottom">
    &copy; 2026 Sunshine Primary School. All rights reserved. | Free to use and share.
  </div>
</footer>

</body>
</html>
