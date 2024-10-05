---
layout: default
title: "El Mockko"
permalink: /el-mockko/
---

Here’s the tool that lets you mockify your text!

<div class="container">
  <h1>El Mockko</h1>
  <textarea id="inputText" rows="4" placeholder="Enter text to mockify"></textarea>
  <input type="text" id="outputText" readonly>
  <button class="btn" onclick="convertText()">Mockify</button>
  <button class="btn" onclick="copyToClipboard()">Copy to Clipboard</button>
  <p id="output"></p>
</div>

<script>
  function convertText() {
      const input = document.getElementById('inputText').value;
      let mockified = '';
      let toggle = true;
      for (let i = 0; i < input.length; i++) {
          let char = input[i];
          if (char.match(/[a-z]/i)) {
              mockified += toggle ? char.toLowerCase() : char.toUpperCase();
              toggle = !toggle;
          } else {
              mockified += char; // keeps spaces, punctuation, etc.
          }
      }
      document.getElementById('outputText').value = mockified;
      document.getElementById('output').textContent = mockified;
  }

  function copyToClipboard() {
      const text = document.getElementById('outputText');
      text.select();
      document.execCommand('copy');
      alert('Copied to clipboard!');
  }
</script>