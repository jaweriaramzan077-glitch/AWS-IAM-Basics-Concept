
# AWS IAM – Access Management Concepts

## 1. IAM User

IAM User ek individual identity hoti hai jo AWS resources ko access karne ke liye use hoti hai. Har user ko specific permissions di ja sakti hain according to uske work.

**Example:** Company mein ek employee ko AWS Console access dena aur usko sirf required resources use karne ki permission dena.

---

## 2. IAM Role

IAM Role ek identity hoti hai jo **temporary permissions** provide karti hai. Role ko directly password ke sath use nahi kiya jata. Users ya AWS services role ko assume karke required resources access kar sakti hain.

**Example:** EC2 instance ko S3 bucket access karwana ho to EC2 ko IAM Role assign kiya ja sakta hai.

---

## 3. IAM Policy

IAM Policy permissions ka set hota hai jo define karta hai ke koi user, role ya service **kya action perform kar sakti hai aur kis resource par**.

**Example:** Ek policy user ko S3 bucket ki files read karne ki permission de sakti hai, lekin files delete karne ki permission nahi.

**Simple:** Policy batati hai **"Who can do what?"**

---

## 4. Principle of Least Privilege

Principle of Least Privilege ka matlab hai ke kisi user ya service ko **sirf utni permissions deni chahiye jitni uske kaam ke liye zaroori hain**.

Extra permissions nahi deni chahiye, kyun ke unnecessary permissions security risk create kar sakti hain.

**Example:** Agar employee ko sirf files read karni hain, to usko files delete karne ki permission nahi deni chahiye.

---

## 5. AWS Root User

AWS Root User woh identity hoti hai jo AWS account create karte waqt automatically create hoti hai. Root User ke paas account ke bohat powerful permissions hoti hain.

Root User ko normal daily tasks ke liye use nahi karna chahiye. Daily work ke liye IAM users, roles ya IAM Identity Center use karna better practice hai.

---

## 6. Why Protect Root User?

Root User ko protect karna bohat important hai because iske paas AWS account par high-level permissions hoti hain.

Agar Root User credentials unauthorized person ke paas chalay jayein, to account ke important resources aur settings affect ho sakti hain.

**Protection:**

* Strong password use karein.
* MFA enable karein.
* Root credentials securely store karein.
* Root User ko daily activities ke liye use na karein.

---

## 7. MFA

**MFA (Multi-Factor Authentication)** account security ki ek extra layer hai.

MFA mein login ke liye password ke sath ek additional verification factor bhi required hota hai.

**Example:**
Password + Authenticator App ka verification code.

Agar kisi ko password pata bhi chal jaye, MFA ki wajah se account ko access karna more difficult ho jata hai.

---

## 8. Root-User-Only Tasks

Kuch specific AWS account-level tasks aise hain jo Root User credentials require kar sakte hain.

**Examples:**

* AWS account close karna.
* Kuch specific account-level settings manage karna.
* Certain account information ya permissions se related tasks.

Is liye Root User ko secure rakhna aur sirf required situations mein use karna important hai.

---

## 9. Federation

**Federation** ka matlab hai users ko unki existing identity ke through AWS resources ka access dena.

Is mein har user ke liye separate AWS password create karne ki zaroorat kam ho sakti hai. User apni organization ki existing identity se authenticate karke AWS access kar sakta hai.

**Example:** Company ke employees apni company login/identity se AWS resources access karte hain.

---

## 10. IAM Identity Center

**IAM Identity Center** AWS accounts aur applications ke access ko centrally manage karne mein help karta hai.

Organization users ko unki **job role aur requirements** ke according access assign kar sakti hai.

**Example:**

* Developer → Development resources ka access
* Administrator → Administrative resources ka access
* Tester → Testing resources ka access

Is se organization mein access management aur user permissions ko centrally manage karna easier hota hai.

---

## Conclusion

AWS IAM ka main purpose **securely manage identities and permissions** karna hai.

IAM User, IAM Role, IAM Policy, Least Privilege, MFA, Federation aur IAM Identity Center ki help se AWS resources ko controlled aur secure way mein access diya ja sakta hai.
