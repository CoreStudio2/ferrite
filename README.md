# 🔥 ferrite - Fast AI Chat on Any Laptop

[![Download ferrite](https://img.shields.io/badge/⬇_Download_ferrite-Latest_Version-blueviolet?style=for-the-badge&logo=github&logoColor=white)](https://github.com/CoreStudio2/ferrite/releases)

ferrite is a small, self-contained program that lets you chat with a powerful AI language model called Qwen 3.5 directly on your own computer. No internet connection is needed after setup, no account is required, and nothing you type ever leaves your machine. It was written from scratch in a programming language called Rust, which is known for being fast and efficient, and it is specially tuned to squeeze every last drop of speed out of ordinary laptop processors. Even on a six-year-old Intel i5 laptop with no graphics card at all, ferrite produces text at roughly 90 tokens per second — which is faster than most people can read.

## 📥 Download and Install

Getting ferrite running on Windows takes just a few minutes. Follow these steps in order.

1. Visit this link to download the application: **https://github.com/CoreStudio2/ferrite/releases**
2. The page that opens lists the available versions, with the newest one at the top. The newest version is always the one you want.
3. Save the file to your computer. Your Downloads folder is a perfectly fine place for it.
4. When the download finishes, open the file you just saved. If Windows shows a blue box saying "Windows protected your PC," click **More info**, then click **Run anyway**. This message appears for many small independent programs and does not mean anything is wrong.
5. Follow the simple on-screen prompts. Accept the default choices unless you have a reason to change them.
6. When setup finishes, ferrite opens automatically. If it does not, look for **ferrite** in your Start menu and click it.

That is the whole process. You do not need to install Python, Rust, a compiler, a code editor, or any extra libraries. Everything ferrite needs is included.

## ✅ What You Need Before You Start

ferrite is designed to run on modest hardware, so most modern Windows laptops and desktops will handle it comfortably.

- **Operating system:** Windows 10 or Windows 11, 64-bit.
- **Processor:** A modern Intel or AMD processor. ferrite takes advantage of advanced processor instructions (including AVX-512 on chips that support it) to go faster, but it also runs well on older chips without them.
- **Memory:** 8 GB of RAM is a comfortable starting point. 16 GB gives you more headroom for longer conversations.
- **Storage:** A few gigabytes of free disk space for the application and the model files.
- **Graphics card:** Not required. ferrite is built specifically for processors, so an integrated graphics chip is completely fine.
- **Internet:** Needed only for the initial download. After that, ferrite works fully offline.

## ✨ What Makes ferrite Special

**Runs entirely on your processor.** Most AI software demands an expensive graphics card. ferrite was built the opposite way — it is a hand-tuned engine that turns your everyday processor into an AI workhorse.

**Built from scratch.** ferrite is not a wrapper around someone else's library. Every part of the engine — how it loads the model, how it schedules work, how it produces text — was written specifically for this project. That is why it can be so fast on hardware that other software struggles with.

**Speculative decoding.** This is a clever technique where the engine makes educated guesses about upcoming words and checks them in batches. When the guesses are right, you get several words for the price of one. The result is a large speed boost that feels instant.

**Private by design.** There is no cloud service, no telemetry, and no login. Your conversations stay on your disk.

**Small and tidy.** ferrite does one job and does it well. There is no bloat, no background updater nagging you, and no unnecessary services running.

## ⚡ Real Performance Numbers

The headline figure is around **90 tokens per second** on a six-year-old Intel i5 laptop with no graphics card. A "token" is roughly three-quarters of a word, so that works out to somewhere in the region of 60 to 70 words per second — comfortably faster than reading speed, which means text appears on screen almost as quickly as you can follow it.

A few things can affect your own numbers:

- **Newer processors** generally run faster, especially those with AVX-512 support.
- **More memory** helps when you work with larger models or longer conversations.
- **Background programs** such as video calls, games, or many browser tabs will slow any processor down, including this one.
- **Power settings** matter more than people expect. Setting Windows to "Best performance" while plugged in can make a noticeable difference.

## 🧠 How It Works in Plain English

When you type a message, ferrite passes it to the Qwen 3.5 model, which lives in a file on your computer. The model reads your words and predicts what should come next, one small piece at a time. ferrite's job is to make those predictions happen as quickly as possible.

It does this with three main tricks. First, it arranges the maths so the processor can work on many numbers at once instead of one at a time — this is where AVX-512 and similar instruction sets come in. Second, it keeps frequently used data close to the processor so it does not have to wait around. Third, it uses speculative decoding to check several candidate words in a single pass. Put together, these tricks turn what would normally be a slow, grinding process into something that feels smooth and responsive.

## 🛠️ Troubleshooting Common Problems

**The download will not start.** Try a different browser. Some browsers block downloads from unfamiliar sources until you confirm you trust them.

**Windows warns me about the file.** Click **More info** and then **Run anyway**. Small independent projects often trigger this message because they have not paid for a commercial code-signing certificate.

**The program opens and then closes immediately.** Restart your computer and try again. If it still happens, make sure you have enough free disk space and that your antivirus is not quarantining a file.

**Responses are slower than expected.** Close other programs, plug in your laptop, and switch Windows power mode to "Best performance." Also check that your laptop is not in a low-power battery-saving state.

**My antivirus flags the file.** Add an exception for the ferrite folder. Because the software is updated frequently, antivirus databases sometimes flag new, rarely-seen programs by mistake.

**Text looks garbled or cuts off.** Start a new conversation. Very long conversations can hit the model's context limit, and starting fresh clears it.

## 💬 Frequently Asked Questions

**Do I need to know how to program?** No. If you can download a file and double-click it, you can use ferrite.

**Does it need the internet?** Only to download it. After that, everything runs locally.

**Will it work on my old laptop?** Very likely. ferrite was specifically built for ordinary processors without graphics cards, and it was tested on a six-year-old i5.

**Is my data sent anywhere?** No. There is no server involved and no account to create.

**Can I use it on Mac or Linux?** The download instructions here cover Windows. Check the releases page for other builds.

**How much does it cost?** Nothing.

## 🎯 Tips for Best Results

- **Be specific.** "Write a 200-word email to my landlord about a broken heater, polite but firm" works far better than "write an email."
- **Give context.** Paste in the text you want summarised or rewritten instead of describing it.
- **Ask for one thing at a time.** Long lists of instructions in a single message produce muddier answers.
- **Start a new conversation** when you switch topics. Old context can bleed into new answers.
- **Keep the model files in one place.** If you move folders around, ferrite may need to be pointed at the model again.

Keywords: avx512, cpu, cpu-inference, inference, inference-engine, inference-optimization, llm, qwen, rust, speculative-decoding