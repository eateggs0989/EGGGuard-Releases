# EGGGuard

**Private File Encryption**

EGGGuard is a private file encryption application designed to protect files using authenticated encryption.


<img width="826" height="550" alt="Screenshot 2026-10-05 195638" src="https://github.com/user-attachments/assets/7349b5c3-8089-4ae3-9f1e-1a86194cc8dd" />


## Why EGGGuard?

**Your secrets should stay your secrets.**

We are EGGGuard — a privacy-focused application built to help you protect the files that matter to you.

Instead of sending your original file directly, EGGGuard places your file inside an encrypted **EGG Container**. The contents are protected with strong encryption, so anyone who gets access to the container cannot read the original file without the correct password.

### Hide Your File Inside an EGG

EGGGuard gives you different ways to package your encrypted data.

For smaller files, **Image Mode** transforms the encrypted container into a normal-looking static image.

The image uses a **1000 × 1000 pixel** structure and can carry encrypted data of approximately **90 KB**. To someone viewing the file, it appears to be an ordinary image — the original file is not directly visible.

If your file is too large for Image Mode, don't worry.

EGGGuard also provides **Text Mode**, which represents the encrypted container as text. The data is protected through multiple layers, including password-based key derivation, authenticated encryption, and encoded container data.

We don't need to expose every internal detail of the implementation here. What matters is simple:

**Your original file is encrypted before it becomes something you can share.**

### Share It Where You Already Share Files

Once your file has been converted into an EGG Container, you can transfer it through platforms that support the resulting file type.

For example, an encrypted image can be shared through services that allow image uploads, while Text Mode can be used where text transfer is more convenient.

You can then send the EGG Container to another person.

The recipient downloads it, opens it with EGGGuard, enters the correct password, and EGGGuard decrypts the container back into the original file.

### Security

EGGGuard uses established cryptographic techniques to protect your files.

- **Scrypt** — derives an encryption key from the user's password.
- **AES-GCM** — encrypts the file data and provides authentication against unauthorized modification.
- **Random salt** — generated for each encrypted container.
- **Random nonce** — generated for each encryption operation.
- **EGG Container** — packages the encrypted data and required metadata.

```text
Your Original File
        │
        ▼
     EGGGuard
        │
        ▼
   Encryption
        │
        ├───────────────┐
        ▼               ▼
   IMAGE MODE        TEXT MODE
        │               │
        ▼               ▼
 Encrypted Image    Encrypted Text
        │               │
        └───────┬───────┘
                ▼
             Share
                │
                ▼
            Recipient
                │
                ▼
            EGGGuard
                │
          Password
                │
                ▼
        Original File 
```

## Supported Platforms

- Windows ---- Live Now You can use freely 
- macOS ---- Not public now 
- Linux ---- Not public now 

## Download

Download the latest version from the [Releases](../../releases) section.

## License

EGGGuard is proprietary software.

You may download and use EGGGuard under the terms of the included license.

You may not copy, modify, redistribute, sell, sublicense, rebrand, or create derivative versions of EGGGuard except where applicable law expressly permits it.

See [LICENSE](LICENSE) for the full terms.
