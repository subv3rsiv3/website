---
layout: pdf-splitter
title: "PDF Splitter"
permalink: /pdf-splitter
---

```
<h2 style="text-align: center">Here’s the tool that lets you mockify your text!</h2>

<div class="el-mockko-container">
  <h2 style="text-align: center;">El Mockko - Text Alternator</h2>

  <label style="text-align: center" for="inputText">Enter Text:</label>
  <textarea style="text-align: center" id="inputText" rows="4" placeholder="Type your text here..."></textarea>

        <!-- Output Area -->
  <label style="text-align: center" for="outputText">Converted Text:</label>
  <input style="text-align: center" type="text" id="outputText" readonly>

        <!-- Action Buttons -->
  <button style="text-align: center; position: sticky; right:80%;" onclick="convertText()">Mockify</button>
  <button style="text-align: center; position: sticky; left:80%;" onclick="copyToClipboard()">Copy to Clipboard</button>
  
  <div style="text-align: center" id="output" class="el-mockko-result"></div>
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
                  mockified += char;
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
```