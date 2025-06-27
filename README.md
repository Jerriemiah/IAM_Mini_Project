# IAM_Mini_Project
---

#  AWS Identity and Access Management (IAM) – My Mini Project Walkthrough

##  **My Understanding of IAM**

During this project, I learned that **IAM (Identity and Access Management)** is like the security control center for everything inside an AWS account. It helps manage **who** can access AWS resources and **what** they’re allowed to do.

To me, IAM felt like having a digital key system for my cloud house. Just like I wouldn’t want to give everyone full access to my home, I realized how IAM helps assign the right level of access to the right people or applications.

It’s a powerful tool that keeps things safe and organized—and it's absolutely essential when working with AWS.

---

##  **Why IAM Is So Important for Security**

I now understand that IAM is **critical for securing data, meeting compliance requirements**, and **controlling access** in a fine-grained way. Here’s what stood out to me:

* IAM ensures only the **right people or services** can access specific AWS resources.
* It prevents **unauthorized access** and data leaks.
* It allows the application of **security best practices**, like **Multi-Factor Authentication (MFA)**, **strong password policies**, and **least-privilege permissions**.

This gave me a clear view of how IAM plays a foundational role in cloud security.

---

## 🧾 **Creating IAM Policies (My Experience)**

One of the hands-on tasks I really enjoyed was creating **custom IAM policies**. These policies are like rulebooks that say what actions are allowed and on which AWS services.

I created two custom policies:

1. `policy_for_eric`: This gave **full access to EC2** services.
2. `development-policy`: This provided **full access to both EC2 and S3** services.

When writing policies, I selected services, actions (like `ec2:*`, `s3:*`), and set them to apply to all resources. Then I reviewed and created them under the **"Customer Managed Policies"** section. I liked how flexible AWS makes policy creation while still keeping it secure and traceable.

---

## 🛠️ **Hands-On Practical: IAM Setup Walkthrough**

### **Part 1: Creating User Eric with EC2 Access**

Here's how I created a user and attached permissions:

1. I opened the **IAM dashboard** from the AWS Console.

2. Went to **Policies** and created `policy_for_eric`:

   * I selected the EC2 service.
   * Granted all actions and all resources.
   * Named it and created the policy.

3. Then, I created a user named **Eric**:

   * Enabled AWS Console access and set a password.
   * Required him to change it on first login.
   * Attached the `policy_for_eric` directly to Eric.

 At this point, Eric had full EC2 access with a secure login.

---

### **Part 2: Creating a Group for Developers and Adding Users**

I also set up a group to manage permissions for multiple users more efficiently:

1. I created a group called **development-team**.
2. Then I created two users:

   * **Jack**
   * **Ade**

While creating each user, I added them directly into the **development-team** group.

3. I created a second policy called **development-policy**:

   * Selected **EC2** and **S3** as services.
   * Granted full access to both.
   * Saved it under "Customer Managed Policies."

4. I attached the **development-policy** to the group `development-team`.

 Now both Jack and Ade have full access to EC2 and S3 through group permissions.

---

##  **What I Learned**

Here are the key takeaways from this mini project:

* I learned how to use **IAM to create users, groups, and policies**.
* I understood the differences between **users vs. roles**, and how to **assign permissions** securely.
* I experienced **policy creation** first-hand, which gave me a deeper understanding of how access control works in AWS.
* I practiced applying **IAM best practices** like:

  * Using groups for scalable permissions
  * Assigning the **least privilege**
  * Using **clear names** and **structured policies**

---

##  **Best Practices I Followed**

During the setup, I made sure to:

*  **Avoid giving unnecessary access**
*  **Use groups to simplify permission management**
*  **Create separate policies** for different roles
*  **Test policies before applying them to real users**
*  **Enforce strong passwords and password resets**
*  **Label and name everything clearly**

This really helped me understand how to keep things clean, manageable, and secure inside AWS.

---

## 🧾 **Final Thoughts**

This project gave me practical experience with one of AWS’s most essential tools. IAM is not just about user creation—it's about **managing identity, access, and security** for everything in the cloud.

I now feel more confident in setting up secure access environments using IAM. Whether I’m giving a user EC2 access or controlling team permissions through groups, I know how to build a safe and organized IAM setup.

---

