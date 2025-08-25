<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Notion-style Toggle</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }
    .toggle {
      cursor: pointer;
      display: flex;
      align-items: center;
      user-select: none;
      margin: 6px 0;
    }
    .arrow {
      transition: transform 0.2s ease;
      margin-right: 8px;
    }
    .content {
      margin-left: 20px;
      display: none;
    }
    .open .arrow {
      transform: rotate(90deg);
    }
    .open .content {
      display: block;
    }
  </style>
</head>
<body>
  <h2>Notion-style Toggle Demo</h2>

  <div class="toggle-item">
    <div class="toggle">
      <span class="arrow">▶</span> Vacation Ideas
    </div>
    <div class="content">
      <ul>
        <li>Eat food</li>
        <li>Hotel</li>
        <li>Swimming</li>
      </ul>
    </div>
  </div>

  <script>
    document.querySelectorAll('.toggle').forEach(toggle => {
      toggle.addEventListener('click', () => {
        toggle.parentElement.classList.toggle('open');
      });
    });
  </script>
</body>
</html>
