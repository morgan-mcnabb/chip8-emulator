# Rust CHIP-8 Emulator

A CHIP-8 emulator written in Rust, featuring audio and graphical display capabilities. This project leverages SDL2 for rendering and keyboard input, and Rodio for audio playback. Emulate classic CHIP-8 programs with ease, customize settings, and enjoy retro gaming on your modern machine.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
  - [Prerequisites](#prerequisites)
  - [Download Executable](#download-executable)
  - [Build from Source (Optional)](#build-from-source-optional)
- [Usage](#usage)
  - [Running the Emulator](#running-the-emulator)
  - [Loading ROMs](#loading-roms)
- [Configuration](#configuration)
  - [Audio Settings](#audio-settings)
  - [Display Settings](#display-settings)
- [Controls](#controls)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

## Features

- **CHIP-8 Instruction Support**: Implements the full CHIP-8 instruction set for accurate emulation.
- **Audio Playback**: Generates and plays sound using Rodio.
- **Graphical Display**: Renders graphics using SDL2 with scalable pixel rendering.
- **Keyboard Input**: Handles keyboard events to interact with CHIP-8 programs.
- **Modular Design**: Clean and modular codebase for easy maintenance and extension.
- **Cross-Platform**: Compatible with major operating systems (Windows, macOS, Linux).

## Installation

### Prerequisites

- **Operating System**: Windows, macOS, or Linux.
- **Rust**: Ensure Rust is installed. If not, install it from [rustup.rs](https://rustup.rs/).
- **SDL2 Libraries**: Required for graphical display and input handling.

  - **Windows**: Download the development libraries from the [SDL2 website](https://www.libsdl.org/download-2.0.php) and place them in the appropriate directories.
  - **macOS**: Install via Homebrew:
    ```bash
    brew install sdl2
    ```
  - **Linux**: Install using your distribution's package manager. For example, on Debian-based systems:
    ```bash
    sudo apt-get install libsdl2-dev
    ```

### Download Executable

1. Visit the [GitHub Releases](https://github.com/yourusername/rust-chip8-emulator/releases) page.
2. Download the latest executable for your operating system (e.g., `chip8-emulator-0.1.exe` for Windows).
3. Create a folder where you want to store the executable.
4. **Optional**: Create a `roms` folder within the executable's directory to store CHIP-8 ROM files.
     ```your-folder/ ├── chip8-emulator-0.1.exe └── roms/ ├── Brick.ch8 ├── Pong.ch8 └── ...other ROMs```

### Build from Source (Optional)

If you prefer to build the emulator from source:

1. **Clone the repository**:
```git clone https://github.com/yourusername/rust-chip8-emulator.git```
2. **Navigate to the project directory**:
`cd rust-chip8-emulator`
3. **Build the project**:
`cargo build --release`
4. The executable will be located in `target/release/`.

## Usage
### Running the Emulator
1. Ensure the SDL2 libraries are correctly installed on your system.
2. Place your CHIP-8 ROM files in the `roms` folder or specify the path when running the emulator.
3. Run the executable:
    - Windows: Double-click `chip8-emulator-0.1.exe` or run it via the command prompt.
    - macOS/Linux:
      `./chip8-emulator-0.1`
4. The emulator will launch and start running the specified ROM.
   
### Loading ROMs
To load a ROM, provide the path to the ROM file as a command-line argument:
`chip8-emulator-0.1 roms/Brick.ch8`
If no ROM is specified, the emulator may attempt to load a default ROM or prompt you to select one.

## Configuration
### Audio Settings
The emulator includes audio playback for specific CHIP-8 instructions. Audio settings can be adjusted in the `audio.rs` module if customization is needed.

### Display Settings
- **Window Dimensions**: The default window size is set to 640x320 pixels, corresponding to the CHIP-8's 64x32 pixel display with a scaling factor.
- **Pixel Scaling**: Adjust the `vram_scale` in `chip8.rs` to change the size of each pixel on the screen.
  
## Controls
- **Exit Emulator**: Press the `Escape key` or close the window.

- **CHIP-8 Keys**: The emulator maps CHIP-8 keys to your keyboard. Below is the default key mapping:

| CHIP-8 Key | Keyboard Key |
| --- | --- | 
| 0 | Num0 |
| 1 | Num1 |
| 2 | Num2 |
| 3	| Num3 |
| 4 |	Num4 |
| 5 | Num5 |
| 6 | Num6 |
| 7 | Num7 |
| 8 | Num8 |
| 9 | Num9 |
| A | A |
| B | B |
| C |	C |
| D | D |
| E | E |
| F |	F |

You can modify the key mapping in the keyboard.rs module if desired.

## Screenshots
_Coming soon!_

## Contributing
Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes with clear and descriptive messages.
4. Push to your fork and submit a pull request.
For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License.

