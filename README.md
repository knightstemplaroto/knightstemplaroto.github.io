# Knights Temoplar OTO
## knightstemplar-oto.org

This is a jekyll site.

### Ruby

Install a Ruby 2.*-ish on your system. rbenv or rvm is recommend to manage multiple ruby versions.

### bundler

Only use bundler to install required gems, via Gemfile.

Once you have a Ruby that works on your system, install dependencies by running `bundler install` in the root of the repository.

### rsync

The helper scripts use `rsync` to deploy. If you are running on a mac, you have `rsync` already.

### SSH keys

Create an SSH key with a password. You likely already have one if you are reading this. Install that key to the authorized keys file on the remote server. In order to avoid disturbing existing authroized keys, use the shell command to copy your key over:

```bash
ssh-copy-id -i ~/.ssh/mykey templarknight@knightstemplar-oto.org
```

**Note:** You will be prompted for the *templarknight*, dreamhost shell user password. This is in the shared passwords database. You should use it once and only once -- to copy your SSH key to the server.

### Local development

* Install Ruby 2.* (ideally use rbenv to manage Ruby version)
* `bundler install`

#### Test locally

* `./serve`

#### Deploy to hosting

* `./deploy`

**Note:** You should have already setup your SSH key for this to work.
