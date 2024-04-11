
## Creation clé

#### Installer gpg : 

```bash
  $ sudo apt update
  $ sudo apt install gnupg
```
Verifier l'installation :
```bash
  $ gpg --version
```

#### Crée la clé privée : 

```bash
  $ gpg --full-generate-key
  $ gpg --list-keys
```

#### Crée la clé public : 

```bash
  $ gpg --output name_of_key_file.gpg --armor --export your.email@example.com
```

#### Ajouter une clé public : 

```bash
  $ gpg --import nom_de_la_cle.asc
```

#### Decrypter un fichier qui a été crypté avec votre clé public : 

```bash
  $ gpg --decrypt fichier.txt.gpg
```

#### Crypter un fichier pour une personne avec sa clé public : 

```bash
  $ gpg --encrypt --sign --recipient "Email_Desitantaire" --output fichier.txt.gpg fichier.txt
```

#### Crypter un fichier pour toutes les personne qui ont votre clé public : 

```bash
  $ gpg --output fichier_signe.txt.sig --sign fichier.txt
```
