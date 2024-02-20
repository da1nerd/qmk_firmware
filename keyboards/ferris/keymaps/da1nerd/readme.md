A usable default keymap for the Ferris keyboard
===============================================

Keymaps in general are quite personal, so it is difficult to come up with a default that will suit every user.

This keymap makes heavy use of keys behaving differently when tapped and held, so that all the keys one may need remain accessible despite the low number of thumb keys.

It comes with a number of layers to give access to most of the keys one may need on a keyboard. It is not meant to be the best possible keymap, but rather a good base on which to build a keymap that works for you.

This is not the only way to make 34 keys a comfortable typing experience, but it is one way to do so. If you don't already know of a better way, this may be as good a starting point as any :)

Note that this keymap was built from the perspective that it is OK to take a steep learning curve if it results in a keymap that is easier to use in the long run. This means that it may take more effort to learn this keymap than some alternatives. "Easy to use" was assessed against the workflow of the author, so your mileage may vary on some of the details.

What do all these layers do?
----------------------------

### Layer 0: Base layer

![Layer 0](./images/layer0.png)

### Layer 1: Symbols

![Layer 1](./images/layer1.png)



### Layer 2: Numbers

![Layer 2](./images/layer2.png)

### Layer 3: Navigation

![Layer 3](./images/layer3.png)

Where is the keymap.c?
----------------------

The keymap.c file is not published to the repository. It is generated from `keymap.json` by the build system.

This avoids duplicating information and allow users to edit their keymap from the qmk configurator web interface.

How do I edit and update the keymap?
------------------------------------

The `keymap.json` file is generated from the [qmk configurator](https://config.qmk.fm) interface and formatted for better readability in the context of the Ferris keyboard.

To edit it, you may:
* Edit it directly from a text editor.
* Edit it from the [qmk configurator](https://config.qmk.fm).

How do I flash the keyboard?
------------------------------------

> Note: you'll need to run the following commands from inside the qmk_firmware directory.

Both halves of the keyboard need to be flash separately. First plug the left side of the keyboard into the computer and run the following command:

```sh
make CONVERT_TO=promicro_rp2040 ferris/sweep:da1nerd:uf2-split-left
```

Wait for the command line to display "Waiting for drive to deploy..." then press the reset button on the keyboard. The process will flash the keyboard and finish automatically.

Next, unplug the left keyboard and plug in the right keyboard and repeat the same process with the following command:

```sh
make CONVERT_TO=promicro_rp2040 ferris/sweep:da1nerd:uf2-split-right
```

Your keyboard is now up to date!
