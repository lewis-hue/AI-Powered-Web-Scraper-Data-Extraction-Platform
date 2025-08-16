title: "Enhanced AI Web Scraper Pro: Project Documentation"
author: "[Your Name]"
date: "r Sys.Date()"
output:
  html_document:
    theme: null
    toc: false
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">

<!-- Inter font (fixed the URL) -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

<!-- Font Awesome -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<style>
/* ========= Design tokens ========= */
:root{
  --bg: #f6f8fb;
  --card: #ffffff;
  --text: #2b3137;
  --muted: #6c757d;
  --accent: #0d6efd;    /* Brand-ish blue */
  --accent-2: #6f42c1;  /* Secondary for gradients */
  --success: #28a745;
  --border: #e9edf3;
  --radius-lg: 16px;
  --radius-md: 12px;
  --shadow-1: 0 6px 24px rgba(0,0,0,.06);
  --shadow-2: 0 30px 80px -25px rgba(13,110,253,.20);
}

@media (prefers-color-scheme: dark){
  :root{
    --bg: #0f172a;
    --card: #0b1220;
    --text: #e5e7eb;
    --muted: #9aa4b2;
    --accent: #8ab4ff;
    --accent-2: #c084fc;
    --success: #34d399;
    --border: #1f2a44;
    --shadow-1: 0 10px 30px rgba(0,0,0,.45);
    --shadow-2: 0 30px 80px -25px rgba(138,180,255,.25);
  }
}

/* ========= Base ========= */
html{ scroll-behavior:smooth; }
::selection{ background: rgba(13,110,253,.2); }
body{
  font-family: 'Inter', system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
  background: radial-gradient(1200px 500px at 50% -200px, rgba(13,110,253,.08), transparent) var(--bg);
  color: var(--text);
  line-height: 1.7;
  -webkit-font-smoothing: antiali
