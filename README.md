# encode64

Extracted from oh-my-zsh. Extended with the decodefile64 function.

Alias plugin for encoding or decoding using `base64` command.

## Functions and Aliases

| Function       | Alias  | Description                              |
| -------------- | ------ | ---------------------------------------- |
| `encode64`     | `e64`  | Encodes given data to base64             |
| `encodefile64` | `ef64` | Encodes given file's content to base64   |
| `decode64`     | `d64`  | Decodes given data from base64           |
| `decodefile64` | `df64` | Decodes given file's content from base64 |

## Usage and examples

### Encoding

- From parameter

  ```console
  $ encode64 "oh-my-zsh"
  b2gtbXktenNo
  $ e64 "oh-my-zsh"
  b2gtbXktenNo
  ```

- From piping

  ```console
  $ echo "oh-my-zsh" | encode64
  b2gtbXktenNo==
  $ echo "oh-my-zsh" | e64
  b2gtbXktenNo==
  ```

### Encoding a file

Encode a file's contents to base64 and save output to text file.  
**NOTE:** Takes provided file and saves encoded content as new file with `.txt` extension

- From parameter

  ```console
  $ encodefile64 ohmyzsh.icn
  ohmyzsh.icn's content encoded in base64 and saved as ohmyzsh.icn.txt
  $ ef64 oh-my-zsh.icn
  ohmyzsh.icn's content encoded in base64 and saved as ohmyzsh.icn.txt
  ```

### Decoding

- From parameter

  ```console
  $ decode64 b2gtbXktenNo
  oh-my-zsh%
  $ d64 b2gtbXktenNo
  oh-my-zsh%
  ```

- From piping

  ```console
  $ echo "b2gtbXktenNoCg==" | decode64
  oh-my-zsh
  $ echo "b2gtbXktenNoCg==" | d64
  oh-my-zsh
  ```

### Decoding a file

Decode a file's base64 encoded content and save output to file.  
**NOTE:** Takes provided file and saves decoded content as new file with stripped extension. (e.g. encoded.txt -> encoded)

- From parameter

  ```console
  $ decodefile64 ohmyzsh.icn.txt
  ohmyzsh.icn.txt's content decoded and saved as ohmyzsh.icn
  $ df64 ohmyzsh.icn.txt
  ohmyzsh.icn.txt's content decoded and saved as ohmyzsh.icn
  ```
