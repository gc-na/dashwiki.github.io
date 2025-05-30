# [डेबियन] Debian Almquist Shell (dash) shift उपयोग: पैरामीटर को स्थानांतरित करना

## Overview
`shift` कमांड का उपयोग शेल स्क्रिप्ट में किया जाता है ताकि कमांड लाइन आर्गुमेंट्स को बाएं की ओर स्थानांतरित किया जा सके। इसका मतलब है कि जब आप `shift` का उपयोग करते हैं, तो पहले आर्गुमेंट को हटा दिया जाता है और बाकी आर्गुमेंट्स एक स्थान पर शिफ्ट हो जाते हैं। 

## Usage
`shift` कमांड का मूल सिंटैक्स निम्नलिखित है:

```bash
shift [n]
```

यहाँ `n` वैकल्पिक है, जो यह निर्दिष्ट करता है कि कितने स्थानों तक शिफ्ट करना है। यदि `n` निर्दिष्ट नहीं किया गया है, तो डिफ़ॉल्ट रूप से 1 स्थान शिफ्ट होता है।

## Common Options
- `n`: यह विकल्प बताता है कि कितने आर्गुमेंट्स को शिफ्ट करना है। यदि आप `shift 2` का उपयोग करते हैं, तो पहले दो आर्गुमेंट्स हटा दिए जाएंगे।

## Common Examples

### Example 1: Basic Shift
```bash
#!/bin/dash
echo "Before shift: $1 $2 $3"
shift
echo "After shift: $1 $2 $3"
```
इस उदाहरण में, पहले आर्गुमेंट को हटा दिया जाएगा और बाकी आर्गुमेंट्स को एक स्थान पर शिफ्ट कर दिया जाएगा।

### Example 2: Shifting Multiple Arguments
```bash
#!/bin/dash
set -- one two three four
echo "Before shift: $1 $2 $3 $4"
shift 2
echo "After shift: $1 $2"
```
यहाँ, पहले दो आर्गुमेंट्स को हटा दिया जाएगा और केवल अंतिम दो आर्गुमेंट्स दिखाए जाएंगे।

### Example 3: Using in a Loop
```bash
#!/bin/dash
set -- apple banana cherry date
while [ "$#" -gt 0 ]; do
    echo "Current fruit: $1"
    shift
done
```
इस स्क्रिप्ट में, सभी आर्गुमेंट्स को एक-एक करके प्रदर्शित किया जाएगा जब तक कि कोई आर्गुमेंट न बचे।

## Tips
- `shift` का उपयोग करते समय ध्यान रखें कि यदि आप अधिक स्थानों को शिफ्ट करने का प्रयास करते हैं जितने आर्गुमेंट्स हैं, तो यह कोई त्रुटि नहीं देगा, लेकिन आर्गुमेंट्स खाली हो जाएंगे।
- स्क्रिप्ट में `shift` का उपयोग करते समय, यह सुनिश्चित करें कि आप सही आर्गुमेंट्स को शिफ्ट कर रहे हैं ताकि आपकी स्क्रिप्ट की कार्यक्षमता प्रभावित न हो।
- `shift` का उपयोग करते समय, आप `"$@"` का उपयोग करके सभी शेष आर्गुमेंट्स को एक साथ संदर्भित कर सकते हैं।