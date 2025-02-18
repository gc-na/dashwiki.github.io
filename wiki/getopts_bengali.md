# [ডেবিয়ান] Debian Almquist Shell (dash) getopts ব্যবহার: অপশন প্রক্রিয়াকরণ

## Overview
`getopts` কমান্ডটি শেলের স্ক্রিপ্টে অপশন প্রক্রিয়াকরণের জন্য ব্যবহৃত হয়। এটি ব্যবহারকারীর দ্বারা প্রদত্ত অপশন এবং তাদের মানগুলি সহজে পরিচালনা করতে সহায়তা করে।

## Usage
`getopts` কমান্ডের মৌলিক সিনট্যাক্স হল:

```sh
getopts optstring variable
```

এখানে `optstring` হল অপশনগুলির একটি স্ট্রিং যা নির্দেশ করে কোন অপশনগুলি গ্রহণযোগ্য এবং `variable` হল সেই ভেরিয়েবল যেখানে অপশনটির মান সংরক্ষিত হবে।

## Common Options
- `-a`: অপশনগুলির জন্য একটি সংক্ষিপ্ত তালিকা তৈরি করে।
- `-n`: স্ক্রিপ্টের নাম নির্দিষ্ট করে।
- `-o`: অপশনগুলির জন্য একটি সংক্ষিপ্ত তালিকা প্রদান করে।

## Common Examples

### উদাহরণ ১: মৌলিক অপশন প্রক্রিয়াকরণ
```sh
#!/bin/dash
while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B with value: $OPTARG"
      ;;
    c)
      echo "Option C with value: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### উদাহরণ ২: অপশন ছাড়া স্ক্রিপ্ট চালানো
```sh
#!/bin/dash
while getopts "a" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### উদাহরণ ৩: একাধিক অপশন গ্রহণ
```sh
#!/bin/dash
while getopts "abc:" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B with value: $OPTARG"
      ;;
    c)
      echo "Option C with value: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

## Tips
- অপশনগুলির জন্য একটি পরিষ্কার এবং সংক্ষিপ্ত স্ট্রিং ব্যবহার করুন যাতে ব্যবহারকারীরা সহজেই বুঝতে পারে।
- `OPTARG` ভেরিয়েবলটি ব্যবহার করে অপশনগুলির মানগুলি সংরক্ষণ করুন।
- স্ক্রিপ্টের শুরুতে একটি সহায়ক বার্তা প্রদান করুন যাতে ব্যবহারকারীরা সঠিকভাবে অপশনগুলি ব্যবহার করতে পারে।