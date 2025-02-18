# [डेबियन] Debian Almquist Shell (dash) getopts उपयोग: विकल्पों को संसाधित करना

## Overview
`getopts` एक शेल बिल्ट-इन कमांड है जिसका उपयोग स्क्रिप्ट में विकल्पों और तर्कों को संसाधित करने के लिए किया जाता है। यह कमांड उपयोगकर्ताओं को कमांड-लाइन विकल्पों को सरलता से प्रबंधित करने की अनुमति देता है।

## Usage
`getopts` का मूल सिंटैक्स इस प्रकार है:

```sh
getopts optstring variable
```

यहाँ `optstring` उन विकल्पों का एक स्ट्रिंग है जिन्हें आप स्वीकार करना चाहते हैं, और `variable` वह नाम है जिसमें विकल्प का मान संग्रहीत किया जाएगा।

## Common Options
- `-a`: सभी विकल्पों को एक साथ संसाधित करने के लिए।
- `-b`: विकल्पों को एक विशेष क्रम में संसाधित करने के लिए।
- `-c`: विकल्पों की गिनती करने के लिए।

## Common Examples

### उदाहरण 1: सरल विकल्प
```sh
#!/bin/sh
while getopts "ab:" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B with value: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### उदाहरण 2: कई विकल्प
```sh
#!/bin/sh
while getopts "xyz" opt; do
  case $opt in
    x)
      echo "Option X selected"
      ;;
    y)
      echo "Option Y selected"
      ;;
    z)
      echo "Option Z selected"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### उदाहरण 3: विकल्पों के साथ तर्क
```sh
#!/bin/sh
while getopts "f:d:" opt; do
  case $opt in
    f)
      echo "File: $OPTARG"
      ;;
    d)
      echo "Directory: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

## Tips
- सुनिश्चित करें कि आप `getopts` का उपयोग करते समय विकल्पों के लिए सही प्रारूप का पालन करें।
- विकल्पों के लिए एक स्पष्ट और संक्षिप्त स्ट्रिंग का उपयोग करें ताकि उपयोगकर्ता आसानी से समझ सकें कि कौन से विकल्प उपलब्ध हैं।
- स्क्रिप्ट में त्रुटियों को संभालने के लिए हमेशा एक डिफ़ॉल्ट केस जोड़ें।