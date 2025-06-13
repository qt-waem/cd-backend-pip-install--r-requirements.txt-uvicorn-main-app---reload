<hr>

<h2>🔍 تحليل الشارت باستخدام الذكاء الاصطناعي</h2>

<form id="upload-form">
  <input type="file" id="image-input" accept="image/*" required />
  <button type="submit">رفع وتحليل الصورة</button>
</form>

<div id="result" style="margin-top: 20px; font-weight: bold;"></div>

<script>
  document.getElementById("upload-form").addEventListener("submit", async function (e) {
    e.preventDefault();
    const input = document.getElementById("image-input");
    if (!input.files.length) return;

    const formData = new FormData();
    formData.append("image", input.files[0]);

    document.getElementById("result").textContent = "جاري التحليل...";

    // نقطة API وهمية الآن – سنربطها لاحقًا
    try {
      const response = await fetch("https://your-ai-endpoint.com/analyze", {
        method: "POST",
        body: formData
      });

      const result = await response.json();
      document.getElementById("result").textContent = "النتيجة: " + result.signal;
    } catch (error) {
      document.getElementById("result").textContent.";
    }
  });
</script>
