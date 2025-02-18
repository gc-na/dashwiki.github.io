# [डेबियन] Debian Almquist Shell (dash) scp उपयोग: फ़ाइलों को सुरक्षित रूप से कॉपी करना

## Overview
`scp` (Secure Copy Protocol) एक नेटवर्क प्रोटोकॉल है जिसका उपयोग फ़ाइलों को एक कंप्यूटर से दूसरे कंप्यूटर पर सुरक्षित रूप से कॉपी करने के लिए किया जाता है। यह SSH (Secure Shell) प्रोटोकॉल पर आधारित है, जिससे डेटा को एन्क्रिप्ट किया जाता है।

## Usage
`scp` कमांड का मूल सिंटैक्स इस प्रकार है:

```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: निर्देशिकाओं को recursively कॉपी करने के लिए।
- `-P`: SSH पोर्ट नंबर निर्दिष्ट करने के लिए (बड़े P के साथ)।
- `-i`: SSH कुंजी फ़ाइल का उपयोग करने के लिए।
- `-v`: विस्तृत आउटपुट दिखाने के लिए, जो डिबगिंग में सहायक होता है।

## Common Examples
1. **स्थानीय मशीन से दूरस्थ मशीन पर फ़ाइल कॉपी करना:**
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. **दूरस्थ मशीन से स्थानीय मशीन पर फ़ाइल कॉपी करना:**
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. **पूर्ण निर्देशिका को दूरस्थ मशीन पर कॉपी करना:**
   ```bash
   scp -r /path/to/local/directory/ user@remote_host:/path/to/remote/directory/
   ```

4. **विशिष्ट SSH पोर्ट का उपयोग करते हुए फ़ाइल कॉपी करना:**
   ```bash
   scp -P 2222 /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

## Tips
- हमेशा सुनिश्चित करें कि आप सही फ़ाइल पथ और उपयोगकर्ता नाम का उपयोग कर रहे हैं।
- यदि आप अक्सर एक ही सर्वर से कनेक्ट करते हैं, तो SSH कुंजी का उपयोग करना बेहतर है ताकि आपको हर बार पासवर्ड दर्ज न करना पड़े।
- `-v` विकल्प का उपयोग करें यदि आपको समस्या निवारण की आवश्यकता है, इससे आपको कनेक्शन प्रक्रिया के बारे में अधिक जानकारी मिलेगी।