---
layout: protocols
title: Set up multiple ssh keys for different GitHub accounts
author: Shaohe Wang
author_url: https://shaohewanglab.org
date: 2022-06-06
---

1. Generate ssh keys following [this instruction](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

    During the process, you will be asked which file to save the key:
    ```
    > Enter a file in which to save the key (/Users/{your_username}/.ssh/id_ed25519): [Press enter]
    ```

    You can use the default private key file name (i.e., id_ed25519) for one of your keys, but you will need to use different names for other keys, and better to be descriptive (e.g., id_lab, or id_{account_name}). At least on Mac, it seems that you have to type out the full path (/Users/{your_username}/.ssh/id_{some_descriptive_name}), but using ~ for home (~/.ssh/id_{some_descriptive_name}) will not work.

1. Adding corresponding SSH keys to your GitHub accounts following [this instruction](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).

1. Create or modify the ssh config file (~/.ssh/config).

    For example, if you have two accounts:
    ```
    Host gh1
      HostName github.com
      User git
      AddKeysToAgent yes
      UseKeychain yes
      IdentityFile ~/.ssh/id_{account_1}
    Host gh2
      HostName github.com
      User git
      AddKeysToAgent yes
      UseKeychain yes
      IdentityFile ~/.ssh/id_{account_2}
    ```

1. Add ssh private keys to your agent following [this instruction](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. Test ssh connections.

    ```bash
    ssh -T git@gh1
    ssh -T git@gh2
    ```

    If it works OK, you should see this message:
    ```
    Hi {account name}! You've successfully authenticated, but GitHub does not provide shell access.
    ```

1. Now you are ready to use the configured gh1 and gh2 hosts for your different GitHub accounts.

    - You can clone your remote repository using `git clone git@gh1:{repo_remote_path} {local_path}` for account_1, or `git clone git@gh2:{repo_remote_path} {local_path}` for account_2.

    - If you have a local repository you want to link to a remote repository, run `git remote add origin git@gh1:{repo_remote_path}` for account_1, or `git remote add origin git@gh2:{repo_remote_path}` for account_2.

    - If you want to update the remote url from using https to using ssh connections, run `git remote set-url origin git@gh1:{repo_remote_path}` for account_1, or `git remote set-url origin git@gh2:{repo_remote_path}` for account_2.
