# Secure Shell (SSH)

<!-- > Created by Fisher at 7:40 PM on 5/19/17. -->

[Secure Shell][wiki-secure-shell] (SSH) is a cryptographic network protocol for operating network services securely over an unsecured network.

## Creates a new public/private rsa ssh key pair, using the provided email as a label.

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

## References

- [Wiki: Secure Shell][wiki-secure-shell], Wikipedia.
- [Generate new ssh key][github-generating-new-ssh-key], Github.

[wiki-secure-shell]: https://en.wikipedia.org/wiki/Secure_Shell "Wiki: Secure Shell"
[github-generating-new-ssh-key]: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/ "Github: Generate new ssh key."
