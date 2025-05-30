# [डेबियन] Debian Almquist Shell (dash) date: समय और तारीख दिखाने के लिए

## Overview
`date` कमांड का उपयोग सिस्टम की वर्तमान तारीख और समय को दिखाने के लिए किया जाता है। यह उपयोगकर्ताओं को विभिन्न प्रारूपों में समय और तारीख को प्रदर्शित करने की सुविधा देता है।

## Usage
कमांड का मूल स्वरूप इस प्रकार है:
```bash
date [options] [arguments]
```

## Common Options
- `+FORMAT`: विशेष प्रारूप में तारीख और समय प्रदर्शित करने के लिए।
- `-u`: यूटीसी (UTC) समय प्रदर्शित करने के लिए।
- `-d STRING`: एक निर्दिष्ट तारीख या समय को प्रदर्शित करने के लिए।

## Common Examples
1. वर्तमान तारीख और समय दिखाने के लिए:
   ```bash
   date
   ```

2. विशेष प्रारूप में तारीख दिखाने के लिए:
   ```bash
   date "+%Y-%m-%d %H:%M:%S"
   ```

3. यूटीसी समय दिखाने के लिए:
   ```bash
   date -u
   ```

4. एक निर्दिष्ट तारीख को प्रदर्शित करने के लिए:
   ```bash
   date -d "2023-10-01"
   ```

## Tips
- `date` कमांड का उपयोग करते समय, सुनिश्चित करें कि आप सही प्रारूप का उपयोग कर रहे हैं ताकि आपको अपेक्षित परिणाम मिल सकें।
- विभिन्न प्रारूपों के लिए `man date` का उपयोग करके अधिक जानकारी प्राप्त करें।