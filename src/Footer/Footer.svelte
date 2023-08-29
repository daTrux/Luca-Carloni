<!-- Footer.svelte -->
<footer class="footer">
    <div class="footer-content">
      <div class="footer-section">
        <h2>Contatti</h2>
        <p>Email: luca.carloni.pt@gmail.com</p>
        <p>Phone: 3479183883</p>
        <p>P. IVA: 12251959965</p>
      </div>
    
    </div>
    <div class="footer-bottom">
      <p>&copy; 2023 Luca Carloni. All rights reserved.</p>
    </div>
  </footer>
  
  <style>
    .footer {
      background-color: #006879;
      color: #fff;
      padding-bottom: 0.5rem;

    }
  
    .footer-content {
      display: flex;
      justify-content: center;
      max-width: 100%;
      margin: 0 auto;
    }
  
    .footer-section {
      /* flex: 1; */
      margin-right: 40px;
    }
  
    .footer-section h2 {
      font-size: 20px;
      margin-bottom: 10px;
    }
  
    .footer-section ul {
      list-style: none;
      padding: 0;
    }
  
    .footer-section li {
      margin-bottom: 5px;
    }
  
    .footer-section a {
      color: #fff;
      text-decoration: none;
    }
  
    .footer-bottom {
      margin-top: 20px;
      text-align: center;
    }
  </style>
  