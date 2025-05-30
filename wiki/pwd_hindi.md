# [डेबियन] Debian Almquist Shell (dash) pwd उपयोग: वर्तमान कार्यशील निर्देशिका दिखाना

## Overview
`pwd` (print working directory) कमांड का उपयोग वर्तमान कार्यशील निर्देशिका का पूर्ण पथ दिखाने के लिए किया जाता है। यह कमांड उपयोगकर्ताओं को यह जानने में मदद करता है कि वे किस निर्देशिका में काम कर रहे हैं।

## Usage
कमांड की मूल संरचना इस प्रकार है:
```
pwd [options] [arguments]
```

## Common Options
- `-L`: यह विकल्प लॉजिकल पथ दिखाता है, जो कि सिम्लिंक को ध्यान में रखता है।
- `-P`: यह विकल्प भौतिक पथ दिखाता है, जो कि सिम्लिंक को नजरअंदाज करता है।

## Common Examples
1. **बुनियादी उपयोग**: वर्तमान कार्यशील निर्देशिका का पथ देखने के लिए:
   ```sh
   pwd
   ```

2. **भौतिक पथ दिखाना**:
   ```sh
   pwd -P
   ```

3. **लॉजिकल पथ दिखाना**:
   ```sh
   pwd -L
   ```

## Tips
- `pwd` कमांड का उपयोग स्क्रिप्टिंग में किया जा सकता है ताकि वर्तमान निर्देशिका को अन्य कमांड में पास किया जा सके।
- जब आप कई सिम्लिंक के माध्यम से नेविगेट कर रहे हों, तो `-P` विकल्प का उपयोग करें ताकि आपको सही भौतिक पथ मिले।