# Password-and-notes-Manager

A Java-based desktop application that provides a simple interface for **generating passwords, storing account credentials, encrypting and decrypting text, and managing personal notes**.

The project is built using **Java Swing and AWT** and also demonstrates the implementation of a **custom hash table with linear probing and rehashing** for password storage.

## 🚀 Features

### 🔑 Password Generator

* Generate random passwords with a user-defined length.
* Uses `SecureRandom` for random password generation.
* Generated passwords can contain:

  * Uppercase letters
  * Lowercase letters
  * Numbers
  * Special characters

### 🔒 Text Encryption & Decryption

* Encrypt text using a secret key.
* Decrypt encrypted text using the same secret key.
* Encrypted output is converted to Base64 for easy viewing and copying.
* Uses Java's built-in cryptography APIs.

### 💾 Password Storage

* Store account names and passwords.
* Search for a password using the account name.
* Delete stored account credentials.
* Uses a custom hash-table implementation instead of Java's built-in `HashMap`.
* Implements linear probing for collision handling.
* Supports rehashing when the table reaches its load threshold.

### 📝 Notes Manager

* Add personal notes.
* Retrieve the most recently added note.
* Notes are managed using Java's `ArrayList`.

### 🖥️ Graphical User Interface

* Built using Java Swing and AWT.
* Interactive buttons and dialog boxes.
* Separate windows for password storage and note creation.
* Startup splash screen with a progress bar.

---

## 🛠️ Technologies Used

| Technology                | Purpose                                 |
| ------------------------- | --------------------------------------- |
| **Java**                  | Core programming language               |
| **Java Swing**            | Graphical User Interface                |
| **Java AWT**              | GUI components and event handling       |
| **SecureRandom**          | Random password generation              |
| **Java Cryptography API** | Encryption and decryption               |
| **Base64**                | Encoding encrypted text                 |
| **ArrayList**             | Notes storage                           |
| **Custom Hash Table**     | Password storage                        |
| **Git & GitHub**          | Version control and source code hosting |

---

## 🧠 Concepts Implemented

This project demonstrates practical implementation of:

* Object-Oriented Programming
* Data Structures
* Hashing
* Hash Tables
* Linear Probing
* Collision Handling
* Rehashing
* Arrays
* ArrayList
* Event Handling
* Exception Handling
* Java Swing
* Java AWT
* Random Password Generation
* Cryptography
* Base64 Encoding

---

## 💻 Requirements

Before running the project, make sure you have the following installed:

### 1. Java Development Kit (JDK)

Install **JDK 8 or later**.

Verify the installation:

```bash
java -version
```

Also verify the Java compiler:

```bash
javac -version
```

### 2. Code Editor / IDE

You can use any Java-compatible editor or IDE.

Recommended options:

* **Visual Studio Code**
* IntelliJ IDEA
* Eclipse

If you are using **Visual Studio Code**, install:

**Extension Pack for Java**

This provides Java language support, debugging, project management, and running Java applications directly from VS Code.

### 3. Git

Git is required to clone the repository.

Verify Git:

```bash
git --version
```

---

## 📦 Additional Dependencies

This project currently does **not require any external libraries or frameworks**.

You do **not** need:

* ❌ Python
* ❌ Node.js
* ❌ MySQL
* ❌ MongoDB
* ❌ Spring Boot
* ❌ Flask
* ❌ Maven
* ❌ Gradle
* ❌ Docker
* ❌ AWS

The application uses Java's built-in libraries such as Swing, AWT, Collections, Security, and Cryptography APIs.

---

## 📥 Installation

### Step 1: Clone the Repository

Open a terminal or command prompt and run:

```bash
git clone https://github.com/yashvardhan06/Password-and-notes-Manager.git
```

### Step 2: Navigate to the Project

```bash
cd Password-and-notes-Manager
```

### Step 3: Open the Project

Open the project folder using your preferred IDE.

For Visual Studio Code:

```bash
code .
```

Make sure the **Extension Pack for Java** is installed.

---

## ▶️ Running the Application

### Using Visual Studio Code

1. Open the project folder in VS Code.
2. Make sure JDK is installed and configured.
3. Open the Java source file containing the `main()` method.
4. Click the **Run** button in VS Code.
5. The application will start with the splash screen.
6. The Password & Notes Manager window will then open.

### Using Terminal

If the Java source file is named `PasswordManager.java`, compile it using:

```bash
javac PasswordManager.java
```

Then run:

```bash
java PasswordManager
```

> If the source filename in your repository is different, compile the Java file containing the `PasswordManager` class and `main()` method.

---

## 🖥️ Application Usage

After launching the application, you can access the following options.

### 1. Generate Password

Click:

```text
GENERATE PASSWORD
```

Enter the required password length.

The application generates a random password containing letters, numbers, and special characters.

---

### 2. Encrypt Text

Click:

```text
ENCRYPT Text
```

You will be asked to enter:

* Text to encrypt
* Secret key

The application generates encrypted text that can be copied and stored.

---

### 3. Decrypt Text

Click:

```text
DECRYPT Text
```

Enter:

* Encrypted text
* Secret key

The application decrypts the text and displays the original content.

---

### 4. Store Password

Click:

```text
STORE PASSWORD
```

Enter:

```text
Account Name
Account Password
```

Click **STORE** to save the credentials.

The credentials are maintained using the application's custom hash-table implementation.

---

### 5. Search Password

Click:

```text
SEARCH PASSWORD
```

Enter the account name.

If the account exists, the corresponding stored password is displayed.

---

### 6. Delete Password

Click:

```text
DELETE PASSWORD
```

Enter the account name to remove the stored credential.

---

### 7. Add Note

Click:

```text
ADD NOTE
```

Enter your note and click **ADD NOTE**.

The note is stored in the application's notes collection.

---

### 8. Get Note

Click:

```text
GET NOTE
```

The application displays the most recently added note.

---

## 🏗️ Project Structure

The project contains several classes responsible for different parts of the application:

```text
Password-and-notes-Manager/
│
├── PasswordManager.java
├── hashTableMap.java
├── background.png
├── key-lock.png
└── README.md
```


## 🔐 Security Implementation

The application contains a `CryptoUtil` class for encryption and decryption.

The current implementation uses:

```text
PBEWithMD5AndDES
```

along with:

* Password-based key generation
* Salt
* Iteration count
* Base64 encoding

The project is primarily intended as an **educational project demonstrating Java cryptography and data structures**.

### ⚠️ Security Notice

The current encryption implementation uses the legacy `PBEWithMD5AndDES` algorithm with a fixed salt and a low iteration count.

Therefore, this project **should not be considered a production-ready password manager** for storing highly sensitive credentials.

For a production application, a modern security design should be used, such as:

* AES-GCM for authenticated encryption
* Argon2id or PBKDF2 for password-based key derivation
* Unique random salts
* Secure persistent encrypted storage
* Master-password authentication

---

## 💾 Data Storage

The current version stores information **in memory**.

### Passwords

Account credentials are stored using a custom hash table:

```text
HashtablePassword
```

The implementatio
