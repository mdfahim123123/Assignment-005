1. Difference between getElementById, getElementsByClassName, querySelector, and querySelectorAll

 এগুলো DOM থেকে element খোঁজার জন্য ব্যবহার হয়।

getElementById
নির্দিষ্ট একটি id দিয়ে element খুঁজে আনে।
সবসময় একটা মাত্র element রিটার্ন করে (কারণ id unique হয়)।

getElementsByClassName("className")
নির্দিষ্ট class নাম দিয়ে multiple elements খুঁজে আনে।
টি একটি HTMLCollection রিটার্ন করে (array-এর মতো কিন্তু পুরোপুরি array নয়)।

querySelector("")
প্রথম matching element রিটার্ন করে।


querySelectorAll("cssSelector")
CSS Selector দিয়ে সব matching elements খুঁজে আনে।
aটি একটি NodeList রিটার্ন করে (যেটা loop করা যায়)।




2. How to Create and Insert a New Element into the DOM

 আমরা createElement দিয়ে element বানাই, তারপর appendChild বা append দিয়ে DOM-এ ঢুকাই।





3. What is Event Bubbling and How it Works

 Event bubbling মানে হলো — যখন কোনো child element-এ event ঘটে, তখন event parent → grandparent → root পর্যন্ত উঠে যায়।


4. What is Event Delegation in JavaScript? Why is it Useful?

 Event Delegation হলো একটি parent element এ event listener বসানো, আর সেই event bubbling এর মাধ্যমে child element-গুলোকে control করা।


একসাথে অনেক child element থাকলে প্রতিটায় আলাদা listener দেওয়ার দরকার হয় না।
New dynamically added element-গুলোও কাজ করবে।


5. Difference between preventDefault() and stopPropagation()

 দুটোই event এর আচরণ নিয়ন্ত্রণ করে, কিন্তু কাজ আলাদা।

preventDefault()
ব্রাউজারের ডিফল্ট অ্যাকশন থামায়।
যেমন: form submit হলে page reload হয় → এটা preventDefault দিয়ে বন্ধ করা যায়।


stopPropagation()
Event bubbling বা capturing থামায়।
মানে parent এ event যাবে না।
