<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>PoC CLEAN - Github Path Typosquat</title>
<style>
body{margin:0;background:#000;color:#fff;font-family:-apple-system,sans-serif;padding:16px;text-align:center}
button{width:100%;max-width:400px;padding:18px;margin:10px auto;display:block;border:0;border-radius:12px;background:#0a84ff;color:#fff;font-size:16px;font-weight:800}
#log{background:#111;color:#0f0;padding:12px;border-radius:10px;font-size:11px;font-family:Menlo,monospace;text-align:left;white-space:pre-wrap;margin:12px auto;max-width:600px;min-height:60px}
</style>
</head>
<body>
<button id="b1">Request Location + redirect to google.com</button>
<div id="log">Log: </div>
<script>
const logEl=document.getElementById('log');
const log = m => logEl.textContent += m + "\n";
logEl.textContent = "URL: " + location.href;

document.getElementById('b1').onclick = () => {
  log("Request location from: " + location.href);
  navigator.geolocation.getCurrentPosition(
    p=>log("GRANTED location"),
    e=>log("Error: "+e.message),
    {timeout:15000}
  );
  setTimeout(()=>{
    log("Redirecting to https://www.google.com ...");
    location.href="https://www.google.com";
  }, 800);
};
</script>
</body>
</html>
