# Macでの環境構築

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install python
brew install ansible
```

```
brew install caskroom/cask/brew-cask
brew cask install vagrant virtualbox
```

## Vagrant

```
vagrant init
vagrant ssh-config >> ~/.ssh/config
vagrant ssh-config --host vagrant >> ~/.ssh/config
vagrant up
```

- `~/.ssh/config`の`Host default`を`Host 192.168.33.*`に書き換える

# Ansibleの疎通確認

## 疎通確認(ローカル)

```
ansible -i local webserver -m ping
```

# Usage

```
ansible-playbook -i local site.yml
```

または

```
export ANSIBLE_HOSTS=./local
ansible-playbook site.yml
```

- 自分の環境に合わせて以下を書き換え
  - local
