<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 600">
  <style>
    @keyframes moveEnemies {
      0% { transform: translateY(0) translateX(0); }
      25% { transform: translateY(20px) translateX(40px); }
      50% { transform: translateY(0) translateX(80px); }
      75% { transform: translateY(-20px) translateX(40px); }
      100% { transform: translateY(0) translateX(0); }
    }
    
    @keyframes moveBoss {
      0% { transform: translateY(0) translateX(0); }
      50% { transform: translateY(20px) translateX(150px); }
      100% { transform: translateY(0) translateX(0); }
    }
    
    @keyframes shootLaser {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(-500px); opacity: 0; }
    }
    
    @keyframes enemyShoot {
      0% { transform: translateY(0); opacity: 0; }
      10% { opacity: 1; }
      100% { transform: translateY(500px); opacity: 0; }
    }
    
    @keyframes explosion {
      0% { opacity: 0; transform: scale(0.2); }
      50% { opacity: 1; transform: scale(1.5); }
      100% { opacity: 0; transform: scale(0.2); }
    }
    
    @keyframes playerMove {
      0% { transform: translateX(0); }
      25% { transform: translateX(100px); }
      50% { transform: translateX(0); }
      75% { transform: translateX(-100px); }
      100% { transform: translateX(0); }
    }
    
    @keyframes starTwinkle {
      0% { opacity: 0.2; }
      50% { opacity: 1; }
      100% { opacity: 0.2; }
    }
    
    @keyframes heavyDamage {
      0% { opacity: 1; }
      25% { opacity: 0.6; }
      50% { opacity: 1; }
      75% { opacity: 0.6; }
      100% { opacity: 1; }
    }
    
    @keyframes shieldPulse {
      0% { opacity: 0.5; transform: scale(1); }
      50% { opacity: 0.8; transform: scale(1.1); }
      100% { opacity: 0.5; transform: scale(1); }
    }
    
    .enemy-group {
      animation: moveEnemies 10s infinite;
    }
    
    .boss {
      animation: moveBoss 8s infinite;
    }
    
    .player-laser {
      animation: shootLaser 2s infinite;
    }
    
    .enemy-laser {
      animation: enemyShoot 3s infinite;
    }
    
    .enemy-laser-2 {
      animation: enemyShoot 3s infinite 1.5s;
    }
    
    .explosion {
      animation: explosion 2s infinite;
    }
    
    .player {
      animation: playerMove 12s infinite;
    }
    
    .star-1 {
      animation: starTwinkle 4s infinite;
    }
    
    .star-2 {
      animation: starTwinkle 6s infinite 1s;
    }
    
    .star-3 {
      animation: starTwinkle 5s infinite 2s;
    }
    
    .damaged-enemy {
      animation: heavyDamage 1s infinite;
    }
    
    .shield {
      animation: shieldPulse 3s infinite;
    }
  </style>
  
  <!-- Enhanced Background with gradient -->
  <defs>
    <radialGradient id="space-background" cx="50%" cy="50%" r="80%" fx="50%" fy="50%">
      <stop offset="0%" style="stop-color:#000033;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#000000;stop-opacity:1" />
    </radialGradient>
    
    <filter id="glow" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur stdDeviation="2" result="blur" />
      <feComposite in="SourceGraphic" in2="blur" operator="over" />
    </filter>
  </defs>
  
  <rect width="800" height="600" fill="url(#space-background)" />
  
  <!-- Enhanced Stars with twinkling -->
  <g>
    <circle class="star-1" cx="100" cy="100" r="1.5" fill="#FFFFFF" />
    <circle class="star-2" cx="200" cy="150" r="2" fill="#FFFFFF" />
    <circle class="star-3" cx="300" cy="80" r="1.8" fill="#FFFFFF" />
    <circle class="star-1" cx="400" cy="120" r="2.5" fill="#FFFFFF" />
    <circle class="star-2" cx="500" cy="200" r="1.7" fill="#FFFFFF" />
    <circle class="star-3" cx="600" cy="90" r="2.2" fill="#FFFFFF" />
    <circle class="star-1" cx="700" cy="180" r="1.6" fill="#FFFFFF" />
    <circle class="star-2" cx="150" cy="250" r="1.9" fill="#FFFFFF" />
    <circle class="star-3" cx="250" cy="220" r="2.1" fill="#FFFFFF" />
    <circle class="star-1" cx="350" cy="280" r="1.8" fill="#FFFFFF" />
    <circle class="star-2" cx="450" cy="240" r="2.3" fill="#FFFFFF" />
    <circle class="star-3" cx="550" cy="300" r="1.5" fill="#FFFFFF" />
    <circle class="star-1" cx="650" cy="270" r="2" fill="#FFFFFF" />
    <circle class="star-2" cx="750" cy="320" r="1.7" fill="#FFFFFF" />
    
    <!-- Add more stars for a richer background -->
    <circle class="star-3" cx="120" cy="350" r="1.2" fill="#FFFFFF" />
    <circle class="star-1" cx="220" cy="50" r="1.9" fill="#FFFFFF" />
    <circle class="star-2" cx="320" cy="380" r="1.5" fill="#FFFFFF" />
    <circle class="star-3" cx="420" cy="410" r="2.1" fill="#FFFFFF" />
    <circle class="star-1" cx="520" cy="70" r="1.8" fill="#FFFFFF" />
    <circle class="star-2" cx="620" cy="390" r="1.4" fill="#FFFFFF" />
    <circle class="star-3" cx="720" cy="430" r="2.2" fill="#FFFFFF" />
  </g>
  
  <!-- Add a distant nebula effect -->
  <ellipse cx="200" cy="150" rx="150" ry="100" fill="#500060" opacity="0.1" />
  <ellipse cx="600" cy="400" rx="180" ry="120" fill="#004080" opacity="0.1" />
  
  <!-- Boss Enemy with glowing effect -->
  <g class="boss" transform="translate(400, 80)">
    <!-- Pixel art Blue Enemy with improved colors and glow effect -->
    <g filter="url(#glow)">
      <rect x="-50" y="-50" width="20" height="20" fill="#0040FF" />
      <rect x="30" y="-50" width="20" height="20" fill="#0040FF" />
      <rect x="-30" y="-30" width="20" height="20" fill="#0040FF" />
      <rect x="10" y="-30" width="20" height="20" fill="#0040FF" />
      <rect x="-50" y="-10" width="20" height="20" fill="#0040FF" />
      <rect x="-30" y="-10" width="20" height="20" fill="#0040FF" />
      <rect x="-10" y="-10" width="20" height="20" fill="#0040FF" />
      <rect x="10" y="-10" width="20" height="20" fill="#0040FF" />
      <rect x="30" y="-10" width="20" height="20" fill="#0040FF" />
      <rect x="-70" y="10" width="20" height="20" fill="#0040FF" />
      <rect x="-50" y="10" width="20" height="20" fill="#0040FF" />
      <rect x="30" y="10" width="20" height="20" fill="#0040FF" />
      <rect x="50" y="10" width="20" height="20" fill="#0040FF" />
      <rect x="-70" y="30" width="20" height="20" fill="#0040FF" />
      <rect x="50" y="30" width="20" height="20" fill="#0040FF" />
      <rect x="-40" y="50" width="40" height="20" fill="#0040FF" />
      <rect x="0" y="50" width="40" height="20" fill="#0040FF" />
      
      <!-- Add eye details for the boss -->
      <rect x="-30" y="-10" width="10" height="10" fill="#FF0000" />
      <rect x="20" y="-10" width="10" height="10" fill="#FF0000" />
    </g>
    
    <!-- Boss health bar -->
    <rect x="-60" y="-70" width="120" height="10" fill="#500000" rx="5" ry="5" />
    <rect x="-60" y="-70" width="90" height="10" fill="#FF0000" rx="5" ry="5" />
  </g>
  
  <!-- Group of Regular Enemies -->
  <g class="enemy-group">
    <!-- Row 1 - Enemy Spaceships (Image 2 - Pixel art with red accents) -->
    <g transform="translate(200, 150) scale(0.6)">
      <rect x="-40" y="-60" width="20" height="20" fill="#000000" />
      <rect x="-20" y="-60" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-60" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-60" width="20" height="20" fill="#000000" />
      <rect x="-60" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-40" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-20" y="-40" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-40" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-40" width="20" height="20" fill="#000000" />
      <rect x="40" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-80" y="-20" width="20" height="20" fill="#000000" />
      <rect x="-60" y="-20" width="20" height="20" fill="#FF0000" />
      <rect x="-40" y="-20" width="20" height="20" fill="#0040FF" />
      <rect x="-20" y="-20" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-20" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-20" width="20" height="20" fill="#0040FF" />
      <rect x="40" y="-20" width="20" height="20" fill="#FF0000" />
      <rect x="60" y="-20" width="20" height="20" fill="#000000" />
      <rect x="-80" y="0" width="20" height="20" fill="#000000" />
      <rect x="-60" y="0" width="20" height="20" fill="#FF0000" />
      <rect x="-40" y="0" width="20" height="20" fill="#0040FF" />
      <rect x="-20" y="0" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="0" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="0" width="20" height="20" fill="#0040FF" />
      <rect x="40" y="0" width="20" height="20" fill="#FF0000" />
      <rect x="60" y="0" width="20" height="20" fill="#000000" />
      <rect x="-60" y="20" width="20" height="20" fill="#000000" />
      <rect x="-40" y="20" width="20" height="20" fill="#FFFFFF" />
      <rect x="-20" y="20" width="20" height="20" fill="#FF0000" />
      <rect x="0" y="20" width="20" height="20" fill="#FF0000" />
      <rect x="20" y="20" width="20" height="20" fill="#FFFFFF" />
      <rect x="40" y="20" width="20" height="20" fill="#000000" />
      <rect x="-40" y="40" width="20" height="20" fill="#000000" />
      <rect x="-20" y="40" width="20" height="20" fill="#FF0000" />
      <rect x="0" y="40" width="20" height="20" fill="#FF0000" />
      <rect x="20" y="40" width="20" height="20" fill="#000000" />
      <rect x="-20" y="60" width="20" height="20" fill="#000000" />
      <rect x="0" y="60" width="20" height="20" fill="#000000" />
    </g>
    
    <!-- Damaged enemy with flickering effect -->
    <g class="damaged-enemy" transform="translate(300, 150) scale(0.6)">
      <rect x="-40" y="-60" width="20" height="20" fill="#000000" />
      <rect x="-20" y="-60" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-60" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-60" width="20" height="20" fill="#000000" />
      <rect x="-60" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-40" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-20" y="-40" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-40" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-40" width="20" height="20" fill="#000000" />
      <rect x="40" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-80" y="-20" width="20" height="20" fill="#000000" />
      <rect x="-60" y="-20" width="20" height="20" fill="#FF0000" />
      <rect x="-40" y="-20" width="20" height="20" fill="#0040FF" />
      <rect x="-20" y="-20" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-20" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-20" width="20" height="20" fill="#0040FF" />
      <rect x="40" y="-20" width="20" height="20" fill="#FF0000" />
      <rect x="60" y="-20" width="20" height="20" fill="#000000" />
      <rect x="-80" y="0" width="20" height="20" fill="#000000" />
      <rect x="-60" y="0" width="20" height="20" fill="#FF0000" />
      <rect x="-40" y="0" width="20" height="20" fill="#0040FF" />
      <rect x="-20" y="0" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="0" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="0" width="20" height="20" fill="#0040FF" />
      <rect x="40" y="0" width="20" height="20" fill="#FF0000" />
      <rect x="60" y="0" width="20" height="20" fill="#000000" />
      <rect x="-60" y="20" width="20" height="20" fill="#000000" />
      <rect x="-40" y="20" width="20" height="20" fill="#FFFFFF" />
      <rect x="-20" y="20" width="20" height="20" fill="#FF0000" />
      <rect x="0" y="20" width="20" height="20" fill="#FF0000" />
      <rect x="20" y="20" width="20" height="20" fill="#FFFFFF" />
      <rect x="40" y="20" width="20" height="20" fill="#000000" />
      <rect x="-40" y="40" width="20" height="20" fill="#000000" />
      <rect x="-20" y="40" width="20" height="20" fill="#FF0000" />
      <rect x="0" y="40" width="20" height="20" fill="#FF0000" />
      <rect x="20" y="40" width="20" height="20" fill="#000000" />
      <rect x="-20" y="60" width="20" height="20" fill="#000000" />
      <rect x="0" y="60" width="20" height="20" fill="#000000" />
    </g>
    
    <g transform="translate(400, 150) scale(0.6)">
      <rect x="-40" y="-60" width="20" height="20" fill="#000000" />
      <rect x="-20" y="-60" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-60" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-60" width="20" height="20" fill="#000000" />
      <rect x="-60" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-40" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-20" y="-40" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-40" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-40" width="20" height="20" fill="#000000" />
      <rect x="40" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-80" y="-20" width="20" height="20" fill="#000000" />
      <rect x="-60" y="-20" width="20" height="20" fill="#FF0000" />
      <rect x="-40" y="-20" width="20" height="20" fill="#0040FF" />
      <rect x="-20" y="-20" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-20" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-20" width="20" height="20" fill="#0040FF" />
      <rect x="40" y="-20" width="20" height="20" fill="#FF0000" />
      <rect x="60" y="-20" width="20" height="20" fill="#000000" />
      <rect x="-80" y="0" width="20" height="20" fill="#000000" />
      <rect x="-60" y="0" width="20" height="20" fill="#FF0000" />
      <rect x="-40" y="0" width="20" height="20" fill="#0040FF" />
      <rect x="-20" y="0" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="0" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="0" width="20" height="20" fill="#0040FF" />
      <rect x="40" y="0" width="20" height="20" fill="#FF0000" />
      <rect x="60" y="0" width="20" height="20" fill="#000000" />
      <rect x="-60" y="20" width="20" height="20" fill="#000000" />
      <rect x="-40" y="20" width="20" height="20" fill="#FFFFFF" />
      <rect x="-20" y="20" width="20" height="20" fill="#FF0000" />
      <rect x="0" y="20" width="20" height="20" fill="#FF0000" />
      <rect x="20" y="20" width="20" height="20" fill="#FFFFFF" />
      <rect x="40" y="20" width="20" height="20" fill="#000000" />
      <rect x="-40" y="40" width="20" height="20" fill="#000000" />
      <rect x="-20" y="40" width="20" height="20" fill="#FF0000" />
      <rect x="0" y="40" width="20" height="20" fill="#FF0000" />
      <rect x="20" y="40" width="20" height="20" fill="#000000" />
      <rect x="-20" y="60" width="20" height="20" fill="#000000" />
      <rect x="0" y="60" width="20" height="20" fill="#000000" />
    </g>
    
    <!-- Row 2 - Blue UFO Enemies -->
    <g transform="translate(250, 230) scale(0.5)">
      <!-- Pixel art Blue Enemy -->
      <rect x="-50" y="-50" width="20" height="20" fill="#0080FF" />
      <rect x="30" y="-50" width="20" height="20" fill="#0080FF" />
      <rect x="-30" y="-30" width="20" height="20" fill="#0080FF" />
      <rect x="10" y="-30" width="20" height="20" fill="#0080FF" />
      <rect x="-50" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="-30" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="-10" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="10" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="30" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="-70" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="-50" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="30" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="50" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="-70" y="30" width="20" height="20" fill="#0080FF" />
      <rect x="50" y="30" width="20" height="20" fill="#0080FF" />
      <rect x="-40" y="50" width="40" height="20" fill="#0080FF" />
      <rect x="0" y="50" width="40" height="20" fill="#0080FF" />
    </g>
    
    <g transform="translate(350, 230) scale(0.5)">
      <!-- Pixel art Blue Enemy -->
      <rect x="-50" y="-50" width="20" height="20" fill="#0080FF" />
      <rect x="30" y="-50" width="20" height="20" fill="#0080FF" />
      <rect x="-30" y="-30" width="20" height="20" fill="#0080FF" />
      <rect x="10" y="-30" width="20" height="20" fill="#0080FF" />
      <rect x="-50" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="-30" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="-10" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="10" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="30" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="-70" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="-50" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="30" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="50" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="-70" y="30" width="20" height="20" fill="#0080FF" />
      <rect x="50" y="30" width="20" height="20" fill="#0080FF" />
      <rect x="-40" y="50" width="40" height="20" fill="#0080FF" />
      <rect x="0" y="50" width="40" height="20" fill="#0080FF" />
    </g>
    
    <g transform="translate(450, 230) scale(0.5)">
      <!-- Pixel art Blue Enemy -->
      <rect x="-50" y="-50" width="20" height="20" fill="#0080FF" />
      <rect x="30" y="-50" width="20" height="20" fill="#0080FF" />
      <rect x="-30" y="-30" width="20" height="20" fill="#0080FF" />
      <rect x="10" y="-30" width="20" height="20" fill="#0080FF" />
      <rect x="-50" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="-30" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="-10" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="10" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="30" y="-10" width="20" height="20" fill="#0080FF" />
      <rect x="-70" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="-50" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="30" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="50" y="10" width="20" height="20" fill="#0080FF" />
      <rect x="-70" y="30" width="20" height="20" fill="#0080FF" />
      <rect x="50" y="30" width="20" height="20" fill="#0080FF" />
      <rect x="-40" y="50" width="40" height="20" fill="#0080FF" />
      <rect x="0" y="50" width="40" height="20" fill="#0080FF" />
    </g>
  </g>
  
  <!-- Player Ship with shield -->
  <g class="player" transform="translate(400, 520) scale(0.8)">
    <!-- Shield effect -->
    <circle class="shield" cx="0" cy="0" r="90" fill="rgba(100, 200, 255, 0.2)" stroke="#40A0FF" stroke-width="2" />
    
    <!-- Player ship -->
    <g filter="url(#glow)">
      <rect x="-40" y="-60" width="20" height="20" fill="#000000" />
      <rect x="-20" y="-60" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-60" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-60" width="20" height="20" fill="#000000" />
      <rect x="-60" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-40" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-20" y="-40" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-40" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-40" width="20" height="20" fill="#000000" />
      <rect x="40" y="-40" width="20" height="20" fill="#000000" />
      <rect x="-80" y="-20" width="20" height="20" fill="#000000" />
      <rect x="-60" y="-20" width="20" height="20" fill="#FF0000" />
      <rect x="-40" y="-20" width="20" height="20" fill="#0040FF" />
      <rect x="-20" y="-20" width="20" height="20" fill="#FFFFFF" />
      <rect x="0" y="-20" width="20" height="20" fill="#FFFFFF" />
      <rect x="20" y="-20" width="20" height="20" fill="#0040FF" />
      <rect x="40" y="-20" width="20" height="20" fill="#FF0000" />
      <rect x="60" y="-20" width="20" height="20" fill="#000000" />
      <rect x="-80" y="0" width="20" height="20" fill="#000000" />
      <rect x="-60" y="0" width="20" height="20" fill="#FF0000" />
      <rect
