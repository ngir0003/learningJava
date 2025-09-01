# Installing Java for LearningJava

This guide provides instructions for installing Java Development Kit (JDK) on your system to start working with Java in the `learningjava` folder.

## Prerequisites
- A computer running Windows, macOS, or Linux.
- Administrative or sudo privileges for installation.
- An internet connection to download the JDK.

## Installation Instructions

### 1. Windows
1. **Download the JDK**:
   - Visit the [Oracle JDK Downloads page](https://www.oracle.com/java/technologies/downloads/) or [OpenJDK Downloads](https://jdk.java.net/).
   - Select the latest JDK version (e.g., JDK 21) for Windows (`.exe` installer).
2. **Install the JDK**:
   - Run the downloaded `.exe` file and follow the installation wizard.
   - Choose the installation directory (default is fine for most users).
   - Ensure the "Set JAVA_HOME variable" option is checked if prompted.
3. **Verify Installation**:
   - Open Command Prompt and run:
     ```
     java -version
     ```
   - You should see output like:
     ```
     java version "21.0.1" 2025-01-14
     ```

### 2. macOS
1. **Download the JDK**:
   - Visit the [Oracle JDK Downloads page](https://www.oracle.com/java/technologies/downloads/) or [OpenJDK Downloads](https://jdk.java.net/).
   - Select the macOS version (`.dmg` or `.tar.gz`).
2. **Install the JDK**:
   - Open the `.dmg` file and follow the installer prompts, or extract the `.tar.gz` file and move it to `/Library/Java/JavaVirtualMachines/`.
3. **Verify Installation**:
   - Open Terminal and run:
     ```
     java -version
     ```
   - Confirm the version output (e.g., JDK 21).

### 3. Linux (Ubuntu/Debian-based)
1. **Install OpenJDK**:
   - Open a terminal and update the package list:
     ```
     sudo apt update
     ```
   - Install the JDK:
     ```
     sudo apt install openjdk-21-jdk
     ```
2. **Verify Installation**:
   - Run:
     ```
     java -version
     ```
   - Ensure the output shows the installed JDK version.

### 4. Set Up Environment Variables (Optional)
To ensure Java is accessible from any terminal session:
- **Windows**:
  - Add `JAVA_HOME` to environment variables (e.g., `C:\Program Files\Java\jdk-21`).
  - Append `%JAVA_HOME%\bin` to the `Path` variable.
- **macOS/Linux**:
  - Add the following to your `~/.bashrc` or `~/.zshrc`:
    ```
    export JAVA_HOME=$(/usr/libexec/java_home)
    export PATH=$JAVA_HOME/bin:$PATH
    ```
  - Reload the shell:
    ```
    source ~/.bashrc
    ```

## Testing Your Setup
1. Navigate to the `learningjava` folder:
   ```
   cd path/to/learningjava
   ```
2. Create a simple Java file, e.g., `Test.java`:
   ```java
   public class Test {
       public static void main(String[] args) {
           System.out.println("Java is working!");
       }
   }
   ```
3. Compile and run:
   ```
   javac Test.java
   java Test
   ```
   - Expected output: `Java is working!`

## Troubleshooting
- If `java -version` returns an error, ensure the JDK is installed and the `JAVA_HOME` and `Path` variables are correctly set.
- For Oracle JDK, you may need an Oracle account to download certain versions.
- Check the [official Java documentation](https://docs.oracle.com/en/java/) for detailed guides.

## Additional Resources
- [Oracle Java Tutorials](https://docs.oracle.com/javase/tutorial/)
- [OpenJDK Documentation](https://openjdk.java.net/)