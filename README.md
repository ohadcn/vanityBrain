vanityBrain
===========

Bitcoin Vanity Address Generation For BrainWallets.

Tired of the random, cryptic addresses generated by regular bitcoin clients? now you can use vanityBrain to create a more personalized address!

Want to have your money always with you? want a rememberable bitcoin account?

This tool will help you get an address, that you and your friends can remember!

requirements
============
This tool is written in python (v2), and depends on coinkit library.

usage
=====
python vanityBrain.py <vanity address starting> [args]

examples
========

look for electrum compatible address, that starts with 1B:

    $ python vanityBrain.py B
    looking for addresses starting with 1B:
    your new key is: angry half quick rant cloud loser into attack shock quietly reveal afraid
    and your address is: 1BSh7VrVHzumkvYkoNaEyQ99tkGEaBaRG9

electrum compatible address, starts with 1B or 1b:

	$ python vanityBrain.py B -i
	looking for addresses starting with 1b:
	your new key is: lift human least quietly talk bring stole smile knee hurt rock mask
	and your address is: 1B6dRPwogCgDPJzhRUDqfCmBUar2aVikzj

	$ python vanityBrain.py B -i
	looking for addresses starting with 1b:
	your new key is: person stuck stomach relationship flirt pound weird companion remind today taint known
	and your address is: 1bVMGoddarpjP6nfEkWtQmpRodjZec5mm

3 english words address, starts with 1B:

	$ python vanityBrain.py B -n -l 3
	looking for addresses starting with 1b:
	Opening dictionary file bip39.txt and validating encoding is utf-8
	finished reading file bip39.txt, starting bruteforce...
	your new key is: snap confirm height 
	and your address is: 1BgNFpbntqfAEQCXLXjAskGHU8fhj13JWD

known issues
============
A. make sure asked address has only base58 acceptable characters (123456789ABCDEFGHJKLMNPQRSTUVWXYZabcdefghijkmnopqrstuvwxyz)

B. estimate time for address generating and notify user of progress.

C. coinkit passphrases seems not to be used by any software, posiible to remove that option?

D. add hive algorythm.
