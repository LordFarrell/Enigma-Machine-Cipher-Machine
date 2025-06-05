# Enigma Machine Cipher Simulator

A fully functional, historically accurate WWII Enigma machine simulator with advanced cryptanalysis tools and educational features. Built as a single HTML file with no external dependencies.

## 🎯 Features

### Core Enigma Functionality
- **5 Historical Rotors** (I-V) with authentic wiring configurations
- **Reflector B** (Wehrmacht standard)
- **Plugboard (Steckerbrett)** supporting up to 10 letter pairs
- **Accurate Rotor Stepping** including the famous double-stepping anomaly
- **Ring Settings (Ringstellung)** for each rotor
- **QWERTZ Keyboard Layout** (authentic German layout)

### Interactive Interface
- **Real-time Encryption/Decryption** with visual feedback
- **Animated Rotor Windows** showing current positions
- **Light Panel** displaying output letters
- **Click-to-Connect Plugboard** with visual cable connections
- **Responsive Design** for desktop and mobile devices

### Educational Mode
- **Step-by-Step Signal Visualization** showing the encryption path
- **Component Animation** highlighting active machine parts
- **Transformation Details** displaying letter changes at each stage
- **Interactive Learning** perfect for understanding Enigma mechanics

### Cryptanalysis Tools
- **Crib Dragging** - Known plaintext attack implementation
- **Brute Force Analysis** - Test all 17,576 rotor positions
- **Plugboard Deduction** - Pattern analysis for suggesting connections
- **Frequency Analysis** - Letter distribution and statistical tests
- **Message History** - Store and retrieve previous encryptions

## 🚀 Quick Start

1. **Download** the `index.html` file
2. **Open** in any modern web browser (Chrome, Firefox, Safari, Edge)
3. **Configure** your machine settings:
   - Select 3 rotors from the available 5
   - Set starting positions (A-Z)
   - Configure ring settings (1-26)
   - Add plugboard connections by clicking letter pairs

4. **Encrypt/Decrypt** messages:
   - Type in the input area or click keyboard keys
   - Watch the output appear letter by letter
   - Use the same settings to decrypt

## 📖 User Guide

### Basic Operation

#### Setting Up the Machine
1. **Choose Rotors**: Select which 3 of the 5 available rotors to use
2. **Set Positions**: Click the position input and type A-Z for each rotor
3. **Ring Settings**: Adjust the ring offset (1-26) for each rotor
4. **Plugboard**: Click two letters to connect them with a cable

#### Encrypting Messages
- **Method 1**: Type directly on the virtual keyboard
- **Method 2**: Enter text in the input area and click "Process Text"
- **Auto-spacing**: Automatically formats output in 5-letter groups
- **Copy Output**: One-click copying of encrypted text

### Advanced Features

#### Educational Mode
Enable to see:
- Signal flow through each component
- Letter transformations at each stage
- Active plugboard connections
- Rotor stepping animations

#### Message History
- Automatically saves last 50 messages
- Timestamps for each encryption
- One-click restoration of any previous machine state
- Export/import capabilities

#### Frequency Analysis
Provides three views:
1. **Input Text Analysis** - Letter frequencies of plaintext
2. **Output Text Analysis** - Letter frequencies of ciphertext
3. **Comparison Mode** - Side-by-side frequency comparison

Statistical measures:
- **Index of Coincidence (IOC)** - Measures text randomness
- **Chi-squared Test** - Compares against English letter frequencies

#### Cryptanalysis Tools

**Crib Dragging**
- Enter known plaintext (crib) and ciphertext
- Finds all positions where the crib could match
- Uses Enigma's non-self-encrypting property
- Essential for breaking messages with known content

**Brute Force Attack**
- Tests all possible rotor positions (17,576 combinations)
- Uses bigram analysis to identify likely plaintext
- Configurable test phrase
- One-click application of discovered settings

**Plugboard Analysis**
- Analyzes letter substitution patterns
- Suggests plugboard connections with confidence scores
- Based on frequency of consistent substitutions
- Helps recover unknown plugboard settings

### Configuration Management

#### Save/Load Settings
- **Save Config**: Store current machine state to browser storage
- **Load Config**: Restore previously saved configuration
- **Export**: Generate base64 configuration code
- **Import**: Load configuration from code

#### Historical Presets
- **Default**: Standard Wehrmacht configuration
- **Wehrmacht Daily Key**: Historical military settings
- **Kriegsmarine Setting**: Naval Enigma configuration

## 🔧 Technical Details

### Implementation
- **Language**: Pure JavaScript (ES6+)
- **Styling**: CSS3 with animations and transitions
- **Structure**: Single HTML file, no external dependencies
- **Storage**: LocalStorage for configuration persistence

### Rotor Specifications
```
Rotor I:    EKMFLGDQVZNTOWYHXUSPAIBRCJ (Notch at Q)
Rotor II:   AJDKSIRUXBLHWTMCQGZNPYFVOE (Notch at E)
Rotor III:  BDFHJLCPRTXVZNYEIWGAKMUSQO (Notch at V)
Rotor IV:   ESOVPZJAYQUIRHXLNFTGKDCMWB (Notch at J)
Rotor V:    VZBRGITYUPSDNHLXAWMJQOFECK (Notch at Z)
Reflector B: YRUHQSLDPXNGOKMIEBFZCWVJAT
```

### Encryption Process
1. **Key Press** → Rotor advancement
2. **Plugboard substitution** (if configured)
3. **Right rotor** encoding
4. **Middle rotor** encoding
5. **Left rotor** encoding
6. **Reflector** substitution
7. **Left rotor** reverse encoding
8. **Middle rotor** reverse encoding
9. **Right rotor** reverse encoding
10. **Plugboard substitution** (if configured)
11. **Output lamp** illumination

### Double-Stepping Mechanism
The simulator accurately implements the mechanical anomaly where:
- When the middle rotor is at its notch position
- And the right rotor steps
- Both the middle AND left rotors advance together

## 🎓 Educational Use

### For Students
- Understand polyalphabetic substitution ciphers
- Learn about historical cryptography
- Practice cryptanalysis techniques
- Explore the relationship between key space and security

### For Educators
- Demonstrate encryption principles visually
- Show the importance of key management
- Illustrate classical cryptanalysis methods
- Discuss the role of cryptography in WWII

### Suggested Exercises
1. **Basic Encryption**: Encrypt your name and decrypt it
2. **Key Recovery**: Given plaintext and ciphertext, find the key
3. **Crib Attack**: Break a message using known plaintext
4. **Frequency Analysis**: Compare encrypted vs. random text
5. **Historical Messages**: Decrypt actual WWII messages

## 🔐 Security Notes

**Historical Context**: The Enigma machine was considered unbreakable during WWII, but was eventually defeated through:
- Mathematical analysis (Polish cryptographers)
- Known plaintext attacks (weather reports, standard phrases)
- Mechanical exploitation (Turing's Bombe)
- Operational errors (repeated message keys, predictable messages)

**Modern Relevance**: While historically significant, Enigma is now purely educational. Its security was based on:
- Large key space (158 quintillion possible settings)
- Daily changing keys
- Additional security through operational procedures

## 🛠️ Troubleshooting

### Common Issues

**Machine won't encrypt**
- Ensure rotors are properly selected (no duplicates)
- Check that positions are valid letters (A-Z)
- Verify ring settings are 1-26

**Plugboard connections not working**
- Click two different letters to connect
- Click a connected letter to disconnect
- Maximum 10 pairs allowed

**Can't decrypt message**
- Ensure exact same settings as encryption
- Rotor positions must match starting positions
- All plugboard connections must be identical

## 📚 Resources

### Further Reading
- "The Enigma Machine" by Simon Singh
- "Seizing the Enigma" by David Kahn
- Bletchley Park Museum resources
- Cryptography textbooks covering classical ciphers

### Historical Information
- Wehrmacht Enigma procedures
- Naval Enigma (4-rotor variant)
- Enigma message formats
- Breaking the Enigma code

## 📄 License

This simulator is provided as-is for educational purposes. Feel free to use, modify, and distribute for non-commercial educational use.

## 🙏 Acknowledgments

- Based on historical Enigma machine specifications
- Inspired by the work at Bletchley Park
- Thanks to the cryptography education community

---

**Remember**: This is a simulator for educational purposes. The actual Enigma machines were mechanical marvels of their time, and the story of breaking their code is one of the greatest intellectual achievements of WWII.
