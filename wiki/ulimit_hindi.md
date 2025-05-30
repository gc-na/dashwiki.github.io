# [डेबियन] Debian Almquist Shell (dash) ulimit उपयोग: संसाधनों की सीमा निर्धारित करना

## Overview
`ulimit` कमांड का उपयोग सिस्टम संसाधनों की सीमाओं को निर्धारित करने के लिए किया जाता है। यह कमांड उपयोगकर्ताओं को यह नियंत्रित करने की अनुमति देता है कि वे कितने संसाधनों का उपयोग कर सकते हैं, जैसे कि मेमोरी, फाइलों की संख्या, और प्रोसेस की सीमाएँ।

## Usage
`ulimit` कमांड का मूल सिंटैक्स इस प्रकार है:

```
ulimit [options] [arguments]
```

## Common Options
- `-a`: सभी सीमाओं को दिखाता है।
- `-c`: कोर फ़ाइल के आकार की सीमा सेट या दिखाता है।
- `-d`: डेटा क्षेत्र के आकार की सीमा सेट या दिखाता है।
- `-f`: फ़ाइल के आकार की सीमा सेट या दिखाता है।
- `-n`: खोले गए फ़ाइलों की अधिकतम संख्या की सीमा सेट या दिखाता है।
- `-s`: स्टैक के आकार की सीमा सेट या दिखाता है।
- `-t`: CPU समय की सीमा सेट या दिखाता है।

## Common Examples
1. सभी सीमाओं को दिखाना:
   ```bash
   ulimit -a
   ```

2. खोले गए फ़ाइलों की अधिकतम संख्या की सीमा सेट करना:
   ```bash
   ulimit -n 1024
   ```

3. कोर फ़ाइल के आकार की सीमा को 0 (कोर फ़ाइलों को निष्क्रिय करने के लिए) पर सेट करना:
   ```bash
   ulimit -c 0
   ```

4. डेटा क्षेत्र के आकार की सीमा को 1GB पर सेट करना:
   ```bash
   ulimit -d 1048576
   ```

## Tips
- ध्यान रखें कि `ulimit` कमांड केवल वर्तमान शेल सत्र के लिए प्रभावी होती है। यदि आप इसे स्थायी रूप से सेट करना चाहते हैं, तो इसे अपने शेल के प्रारंभिक स्क्रिप्ट में जोड़ें।
- सीमाओं को बढ़ाने से पहले सुनिश्चित करें कि आपके सिस्टम पर पर्याप्त संसाधन उपलब्ध हैं।
- सिस्टम की सुरक्षा और स्थिरता बनाए रखने के लिए सीमाओं को उचित रूप से सेट करें।