# Installing Flutter

{% hint style="danger" %}
If you have an administered system, your administrator should have already performed these steps! Otherwise, you'll need to get into contact with them to do so.
{% endhint %}

In order to use Flutter, we first have to install it onto our computers. You will need to have VS Code open for this.

## Downloading and Installing

{% hint style="info" %}
Note that these directions assume you are using macOS. If you are using Windows or Linux, follow the [official directions](https://flutter.dev/docs/get-started/install/windows).
{% endhint %}

* [Download Flutter](https://storage.googleapis.com/flutter_infra/releases/stable/macos/flutter_macos_1.22.4-stable.zip). It'll take a while to download because it's a pretty large file.
* Unzip the file you just downloaded like you did with VS Code. A new folder called "flutter" should be created. Make sure it's in your Downloads folder.

Now, you'll need to have VS Code open.

* In the menu bar, go to Terminal, then select New Terminal.
* Type the following commands and click enter after each one:
  * `cd ~/Downloads`
  * `mv flutter ~/flutter`
    * \(this one might take a while\)
  * `code ~/.zshrc`
* A new window should open in VS Code. This is a _text editing_ window.
* Scroll to the bottom of the file and make a new line \(hit the enter button\). Then, type:
  * `export PATH="$PATH:$HOME/flutter/bin"`
* Return back to the terminal and enter the following commands:
  * `source ./zshrc`
  * `which flutter`

If you don't get a message that says "flutter not found", then congratulations, you've installed Flutter!

