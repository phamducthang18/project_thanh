<template>
  <footer>
    <div class="footer-container">
      <div class="footer-content">
        <!-- About Us -->
        <div class="footer-about">
          <h4>About Us</h4>
          <p>We provide excellent services in various sectors. Explore our services and join us!</p>
        </div>

        <!-- Quick Links -->
        <div class="footer-links">
          <h4>Site Map</h4>
          <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/services">Services</a></li>
            <li><a href="/contact">Contact Us</a></li>
            <li><a href="/about">About Us</a></li>
          </ul>
        </div>

        <!-- Company Info -->
        <div class="footer-company">
          <h4>Company Info</h4>
          <p><strong>Company:</strong> LongWall Asia Pacific</p>
          <p><strong>Address:</strong> Lane 68, Trieu Khuc, Tan Trieu Commune, Thanh Tri District, Hanoi City, Vietnam</p>
          <p><strong>Phone:</strong> <a href="tel:+84969988247">0969 988 247</a></p>
          <p><strong>Email:</strong> <a href="mailto:support@longwall.asia">support@longwall.asia</a></p>
        </div>
      </div>

      <!-- Footer Bottom -->
      <div class="footer-bottom">
        <p>&copy; 2025 LongWall Asia Pacific. All Rights Reserved.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
footer {
  background-color: #2c3e50;
  color: #fff;
  padding: 40px 0;
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  width: 100%;
  gap: 20px;
}

.footer-about,
.footer-links,
.footer-company {
  width: 30%;
}

h4 {
  font-size: 18px;
  margin-bottom: 12px;
}

.footer-about p,
.footer-company p {
  font-size: 14px;
  margin-bottom: 8px;
}

.footer-links ul {
  list-style-type: none;
  padding: 0;
}

.footer-links ul li {
  margin: 8px 0;
}

.footer-links ul li a {
  color: #fff;
  text-decoration: none;
}

.footer-links ul li a:hover {
  text-decoration: underline;
}

.footer-company p a {
  color: #f1c40f;
  text-decoration: none;
}

.footer-company p a:hover {
  text-decoration: underline;
}

.footer-bottom {
  text-align: center;
  margin-top: 20px;
  padding-top: 10px;
  border-top: 1px solid rgba(255, 255, 255, 0.2);
}

.footer-bottom p {
  font-size: 14px;
}
</style>
