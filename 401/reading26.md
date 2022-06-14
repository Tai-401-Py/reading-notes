# API Deployment

## [Managing Django](https://djangostars.com/blog/configuring-django-settings-best-practices/)

Sensitive data: You have a secret key in each project, on top of this there can be third party tokens that can not be stored in VCs. 

`settings_local.py` 

Pros: Can have debug on while working, it's run only locally so it doesn't affect your production settings. Secrets not in Version Control System (VCS).

Cons: It's not in the VCS so you can lose settings switching to prod. you also need to have the local_settings shared across all developers. 


### Using seperate Settings files for each environment

Pros: All environments are in a VCS, It's easy to share between devs.

Cons: Still need to handle secrets and tokens somehow, inheritance of settings can be difficult to maintain.

### The `.ENV` 

This solves most issues with sensitive data.  However you then need to handle `KEYERROR` exceptions.

PROS: Configuration is separated from code, You have the same code for all environments, No inheritance in settings, and cleaner and more consistent code.

There is a theoretical grounding for using environment variables/

Cons: you need to handle sharting of the config between devs. 

## Naming Conventions

- Give meaningful names to your settings.
- Always use the prefix with the project name for your custom (project) settings.
- Write descriptions for your settings in comments.

---

## [SSH](https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work)

(SSH) Secure Shell Protocol, is a remote administration protocol that allows users to access, control, and modify their remote servers over the internet.

### How do it do the thing?

SSH commands consist of three major parts

`ssh {user}@{host}`

`{user}` - The account you want to access
`{host}` - The computer or webserver you want to access

It is after this info is entered you will be prompted for a password, it will not appear as you type but it is being transmitted. If correct, you'll get a remote terminal window. 

### Understanding the Encryption

There are three different encryption technologies used by SSH:

- Symmetrical encryption: also knowm as a shared key or shared secret, the process is carried out by a key exchange algorithm and can encrypt entire communications. 
- Asymmetrical encryption: Also known as a public/private key pair. A message is sent with a specific users private key and can be decrypted only using the correct users public key. Once a secured symmetric communication has been established, the server uses the client’s public key to generate and challenge and transmit it to the client for authentication. If the client can successfully decrypt the message, it means that it holds the private key required for the connection – the SSH session then begins.
- Hashing: SSH uses hashes to verify the authenticity of messages. This is done using HMACs, or Hash-based Message Authentication Codes. This ensures that the command received is not tampered with in any way.

### Session Encryption Negotiation

When a client tries to connect via TCP  the server presents a protocol. If the client has a matching protocol, an agreement is reached and the session begins. 

At it's core it's 6 steps.

1. Pick a large prime creating a **Seed Value**
2. Agree on a common encryption method
3. Generate a second prime number to serve as a **Private Key**
4. With the private key and agreedencryption alo9nwith the shared number, they compute a **public key**
5. The parties then use a personal private key, the shared public key, and the OG prime to create a final **shared key**
6. With the Shared key they can now encrypt and decrypt each others communications. 