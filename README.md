# Python Obfuscator

A versatile tool for obfuscating Python code using a variety of techniques, including custom methods and contributions from the community. This tool is designed to make your Python code highly resistant to reverse engineering while ensuring that it remains fully functional for execution.

# Key Features

- Obfuscation Layers: Apply multiple layers of encryption and encoding to make code virtually unreadable to humans while remaining interpretable by machines.
- Modular Architecture (Version 2): Easily expandable with custom modules to fit your specific needs.
- Integrated Tools: Includes optional features like error encryption and virtual machine (VM) detection for enhanced security.

# Version Updates
Version 2.4
- Added the Kramer obfuscation method as an external module (#3).
- Implemented a version checker to ensure compatibility between the repository and client versions.
Version 2
- Transitioned to a modular design for better scalability and customization.
- Introduced additional tools, including error encryption and VM detection, all of which can be configured to your preferences.

# Obfuscation Options
Obfuscation Layers
Each layer provides a unique level of encryption or encoding to protect your code:

Layer 1: Initial Base64 encoding.

Layer 2: Combines binary encryption and list-based encoding.

Layer 3: Code splitting using patterns of 1 and i.

Layer 4: Secondary Base64 encoding with a modified approach.

Layer 5: Pickle serialization to obscure readability.

Layer 6: Pickle serialization with anti-tamper functionality; the deserialized code checks for tampering.

# External Layers:

- py_fuscate method
- wodx_obfuscate method
- Kramer method

# Configuration Options

custom_input (True/False): Determines whether to input the code from a custom file (True) or use a variable (False).

custom_output (True/False): If True, specifies a custom filename for the obfuscated output. If False, outputs as obfuscated.py, overwriting any existing file with the same name.

speed_test (True/False): Runs a subprocess to compare performance between standard and AST-based obfuscation. (Primarily for debugging purposes.)

add_vm_detection_to_script (True/False): Inserts VM detection code at the beginning of your script. Refer to vmcheck_code.txt for more details.

minify_original_code (True/False): Minifies your code to reduce its size, serving as an additional obfuscation layer.

add_error_encryption (True/False): Encrypts error messages, generating a private_key.pem for decryption. Use error_decoder.py to view the errors during debugging.

do_ast_encrypt (True/False): Applies AST-based encryption for heightened security. Note: This can significantly slow down execution and is considered experimental.

var_type (1, 2, or 3): Specifies the naming convention for variables:

1 = Numeric (1, 0)

2 = Alphanumeric (I, 1)

3 = Alphabetic (O, 0)

This tool is designed with flexibility and customization in mind. While the documentation and variable names are subject to improvement, the functionality delivers robust protection for your Python scripts.
