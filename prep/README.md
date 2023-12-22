# Encrypted notes

M'n eerste personal use README. 'tiswat

## Wat zijn dit?

Alles in de map encrypted is sowieso encrypted
De lest moet los defined worden

Of, natuurlijk, is openbaar.

## Hoe gebruik ik ze?

### Transcrypt

#### Per systeem	

	$ git clone https://github.com/elasticdog/transcrypt.git
	$ cd transcrypt/
	$ sudo ln -s ${PWD}/transcrypt /usr/local/bin/transcrypt

#### Per repo

	transcrypt
	Y
	'Password'

#### Per cloned repo

Na het clonen van een encrypted repo doet aan de zendkant:
	--display
Want dan krijg je de informatie en een commando voor ontvangkant
	$ transcrypt --display
	The current repository was configured using transcrypt v0.2.0
	and has the following configuration:

	  CONTEXT:  default
	  CIPHER:   aes-256-cbc
	  PASSWORD: correct horse battery staple

	Copy and paste the following command to initialize a cloned repository:

	 transcrypt -c aes-256-cbc -p 'correct horse battery staple'
Die laatste is dus pittig relevant!

### belangrijk: 

	$ cd <path-to-your-repo>/
	$ echo 'sensitive_file  filter=crypt diff=crypt merge=crypt' >> .gitattributes
	$ git add .gitattributes sensitive_file
	$ git commit -m 'Add encrypted version of a sensitive file'

Want dat zorgt ervoor dat ze ook ge-encrypt worden.
NB: 
The .gitattributes file should be committed and tracked along with everything else in your repository so clones will be aware of what is encrypted. Make sure you don't accidentally add a pattern that would encrypt this file :-)
