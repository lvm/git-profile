# git-profile

Setup easily a profile for git-config

Note that you can alternatively use `includeIf` in your `~/.gitconfig`, like so:

```
; include for all repositories inside $HOME/to/group
[includeIf "gitdir:~/work/"]
	path = ~/.gitconfig-work
```

```
# ~/.gitconfig-work

[core]
	sshCommand = ssh -i ~/.ssh/work/id_ed25519
[user]
	name = Walter White
	email = walter@greymatter.com
```


## Usage

```
cd ~/work/something \
  && git-profile --ssh ~/.ssh/work/id_ed25519 \
  && git-profile --name "Mauro L" \
  && git-profile --email "mauro@example.com"
```

```
cd ~/hobbies/something-else \
  && git-profile --ssh ~/.ssh/id_ed25519 \
  && git-profile --name "Cool Dude" \
  && git-profile --email "cooldude@example.com"
```

```
cd ~/hobbies/shady \
  && git-profile --ssh ~/.ssh/id_ed25519 \
  && git-profile --name "Anon" \
  && git-profile --email "askbill@microsoft.com"
```

## License

BSD 3-Clause
