<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Copywriting App</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 flex items-center justify-center min-h-screen">
  <div class="bg-white p-8 rounded-2xl shadow-lg w-full max-w-md">
    <h1 class="text-2xl font-bold mb-4 text-center text-indigo-600">Copywriting Generator ✨</h1>

    <textarea id="input" class="w-full p-3 border rounded-lg mb-4 focus:ring-2 focus:ring-indigo-400" placeholder="Masukkan produkmu..."></textarea>

    <button onclick="generateCopy()" class="w-full bg-indigo-600 text-white py-2 rounded-lg hover:bg-indigo-700 transition">
      Generate Copywriting
    </button>

    <div id="output" class="mt-4 p-3 border rounded-lg bg-gray-50 text-gray-700 min-h-[100px]"></div>

    <button onclick="copyText()" class="mt-3 w-full bg-green-500 text-white py-2 rounded-lg hover:bg-green-600 transition">
      Copy Teks
    </button>
  </div>

  <script>
    function generateCopy() {
      const input = document.getElementById("input").value.trim();
      const output = document.getElementById("output");
      if (input === "") {
        output.innerText = "❌ Masukkan nama produk dulu!";
        return;
      }
      output.innerText = `🚀 Nikmati ${input} terbaikmu sekarang juga! Kualitas premium dengan harga spesial. Yuk, cobain hari ini juga ✨`;
    }

    function copyText() {
      const text = document.getElementById("output").innerText;
      navigator.clipboard.writeText(text);
      alert("Teks berhasil disalin ✅");
    }
  </script>
</body>
</html>
