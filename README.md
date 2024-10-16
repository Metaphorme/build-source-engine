# Build Source Engine

Build source engine from [nillerusr/source-engine](https://github.com/nillerusr/source-engine).

## Status

| Badge | Meaning |
| --- | --- |
| ✅ | Work well! |
| ❓ | Haven't been tested. |
| ❌ | Can't work! |

<table>
	<tr>
	    <th colspan="5">Status</th>
	</tr >
  
  <tr>
    <td>Platform</td>
    <td>Status</td>
    <td>Architecture</td>
    <td>Game</td>
  </tr>
  
  <tr>
    <td rowspan="8">macOS</td>
    <td rowspan="8">
	<a href="https://github.com/Metaphorme/build-source-engine/actions/workflows/build-for-macos.yml"><img src="https://github.com/Metaphorme/build-source-engine/actions/workflows/build-for-macos.yml/badge.svg" alt="Build for macOS"></a>
    	<br>
	<a href="https://github.com/Metaphorme/build-source-engine/actions/workflows/test-for-macos.yml"><img src="https://github.com/Metaphorme/build-source-engine/actions/workflows/test-for-macos.yml/badge.svg" alt="Test for macOS"></a>
    </td>
    <td rowspan="4">AArch64</td>
    <td>hl2</td>
  </tr>
  <tr>
    <td>episodic</td>
  </tr>
  <tr>
    <td>hl1</td>
  </tr>
  <tr>
    <td>portal</td>
  </tr>
  <tr>
    <td rowspan="4">x86_64</td>
    <td>hl2</td>
  </tr>
  <tr>
    <td>episodic</td>
  </tr>
  <tr>
    <td>hl1</td>
  </tr>
  <tr>
    <td>portal</td>
  </tr>

  <tr>
    <td rowspan="8">Linux</td>
    <td rowspan="8">
	<a href="https://github.com/Metaphorme/build-source-engine/actions/workflows/build-for-linux.yml"><img src="https://github.com/Metaphorme/build-source-engine/actions/workflows/build-for-linux.yml/badge.svg" alt="Build for Linux"></a>
    	<br>
	<a href="https://github.com/Metaphorme/build-source-engine/actions/workflows/test-for-linux.yml"><img src="https://github.com/Metaphorme/build-source-engine/actions/workflows/test-for-linux.yml/badge.svg" alt="Test for Linux"></a>
    </td>
    <td rowspan="4">x86_64</td>
    <td>hl2</td>
  </tr>
  <tr>
    <td>episodic</td>
  </tr>
  <tr>
    <td>hl1</td>
  </tr>
  <tr>
    <td>portal</td>
  </tr>
  <tr>
    <td rowspan="4">i386</td>
    <td>hl2</td>
  </tr>
  <tr>
    <td>episodic</td>
  </tr>
  <tr>
    <td>hl1</td>
  </tr>
  <tr>
    <td>portal</td>
  </tr>

  <tr>
    <td rowspan="8">Android</td>
    <td rowspan="4">
	<a href="https://github.com/Metaphorme/build-source-engine/actions/workflows/build-for-android.yml"><img src="https://github.com/Metaphorme/build-source-engine/actions/workflows/build-for-android.yml/badge.svg" alt="Build for Android"></a>
    </td>
    <td rowspan="4">ARMv7a</td>
    <td>hl2</td>
  </tr>
  <tr>
    <td>episodic</td>
  </tr>
  <tr>
    <td>hl1</td>
  </tr>
  <tr>
    <td>portal</td>
  </tr>
  <tr>
    <td rowspan="4">❌</td>
    <td rowspan="4">ARMv8</td>
    <td>hl2</td>
  </tr>
  <tr>
    <td>episodic</td>
  </tr>
  <tr>
    <td>hl1</td>
  </tr>
  <tr>
    <td>portal</td>
  </tr>
  
</table>

## How to play (using Half-Life 2 as an example)

[中文教程](https://diazepam.cc/post/play-halflife2-natively-on-apple-silicon/)

### Download game files

Buy and download [Half-Life 2 from Steam](https://store.steampowered.com/app/220/HalfLife_2/).

### Add the engine files

Download correct engine from [release page](https://github.com/Metaphorme/build-source-engine/releases), uncompress and add **files** into corresponding game files' directory.

### Launch

Run:

```bash
DYLD_LIBRARY_PATH=bin/ ./hl2_launcher
````

## Known bugs

1. If it can't display Chinese or other languages in the menu and subtitles, you can set the menu and subtitles to English while using the native audio.
   
   Just launch as follows:
   
   ```bash
   # language       ->  Interface
   # audiolanguage  ->  Audio
   # cc_lang        ->  Subtitles
   DYLD_LIBRARY_PATH=bin/ ./hl2_launcher -language english -audiolanguage schinese +cc_lang english
   ```

   For more information, please [check](https://steamcommunity.com/sharedfiles/filedetails/?id=3089088861).
