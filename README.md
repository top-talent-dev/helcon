 ## Overview

The Helcon Application is a web-based system designed to facilitate communication and management between doctors and patients within a healthcare environment. It provides features for doctors to schedule appointments, send messages, and manage patient records. Patients can register, view appointments, receive messages, and access their medical records through the application
The application is built using Rust programming language with the Internet Computer (IC) Canister SDK, providing a secure and decentralized platform for healthcare data management. It utilizes stable data structures for efficient storage and retrieval of patient information, appointments, messages, and medical records.




## Setting Up the Project <a name="setup"></a>

To set up and start working on the Doctor-Patient Application project, follow these steps:



### 1. Install Rust and Dependencies

- Ensure you have Rust installed, version 1.64 or higher. You can install it using the following commands:

  ```bash

  $ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh

  $ source "$HOME/.cargo/env"

  ```

- Install the `wasm32-unknown-unknown` target:

  ```bash

  $ rustup target add wasm32-unknown-unknown

  ```

- Install `candid-extractor`:

  ```bash

  $ cargo install candid-extractor

  ```



### 2. Install DFINITY SDK (`dfx`)

- Install `dfx` using the following commands:

  ```bash

  $ DFX_VERSION=0.15.0 sh -ci "$(curl -fsSL https://sdk.dfinity.org/install.sh)"

  $ echo 'export PATH="$PATH:$HOME/bin"' >> "$HOME/.bashrc"

  $ source ~/.bashrc

  $ dfx start --background

  ```



### 3. Update Dependencies

- Update the `dependencies` block in `/src/{canister_name}/Cargo.toml` with the required dependencies.



### 4. Autogenerate DID

- Add the provided script to the root directory of the project.

- Update line 16 with the name of your canister.

- Run the script each time you modify/add/remove exported functions of the canister.



### 5. Running the Project Locally

- Start the replica, running in the background:

  ```bash

  $ dfx start --background

  ```

- Deploy your canisters to the replica and generate your Candid interface:

  ```bash

  $ npm run gen-deploy

  ```
