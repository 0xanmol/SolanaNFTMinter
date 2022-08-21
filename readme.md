# Welcome to SolanaNFTMinter
# Getting started

We will be installing Rust, Solana and Anchor
Either watch [this](https://www.youtube.com/watch?v=ROOT-lQN5AY&t=714s) video or follow the commands listed below. 

It is necessary for me to tell you that regardless of me doing my best to cover all edge cases and providing you all the solutions during this installation process, setting up dev envioments is frustrating. Have fun :)

## For Mac/Linux:
###  To install Rust
   ```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
check if you have installed everything correctly by typing this in the terminal
``````
rustc -V or rustc --version
``````
and also check for cargo, which is the package manager for rust
```cargo -V or cargo --version```

2nd thing we are going to install is Solana
### To install Solana
```sh -c "$(curl -sSfL https://release.solana.com/v1.10.32/install)"```
> **Note:** you might be promted to add solana to your \$PATH on your screen after this step, do so by following the steps on your screen, I'll leave the command here too!
```export PATH="/home/YOUR_SYSTEM_NAME/.local/share/solana/install/active_release/bin:$PATH"```

Check if it was succesful by typing ```$PATH``` in your terminal

Check the version of solana installed by typing ```Solana --version```

You can check your Solana wallet address by typing ```Solana address```
If you face an error after doing so, create a new wallet by typing
```solana-keygen new```

### Installing Anchor
This is the most pain in the ass thing ever. now that I have stated that, let's get started 
```cargo install --git https://github.com/project-serum/anchor avm --locked --force```

After that's done, install the latest version of 'AVM' or the Anchor Version Manager:
```avm install latest```
and then,
```avm use latest```

Finally, check the latest version of Anchor by typing
```anchor --version```

All of this might seem pretty straightforward, your life might seem happy and simple now. Huh, naive lil kid

Just to play around you can create a new Anchor project by typing
```
mkdir AnchorTest
cd AnchorTest
anchor init
```
now go explore all the files created by anchor in the template project. It usually contains an app folder for your client-side application. Migrations folder for deploy scripts, tests folder for obv, tests and the programs folder contains the lib.rs, the smart contract!



