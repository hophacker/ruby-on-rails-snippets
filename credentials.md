#### master key V.S. secret_ key base
Rails master key is used to decrypt credentials in a running rails instance(mostly production mode), while secret key base is used for issuing rails secrets when for example, delivering cookies.
Rails master key is defined by providing a file named `config/master.key` or by attatching env with name `RAILS_MASTER_KEY`.
Secret key base is defined by putting it in encrypted credential with name `secret_key_base` or by attatching env with name `SECRET_KEY_BASE`.

It is a big fault if rails master key appears at your codebase, instead, you can store it in
* A secret base, ex., encrypted cloud storage
* Your docker deployment yaml with environment name: `RAILS_MASTER_KEY`

#### Help
`rails credentials:help`

#### Edit
* Before editing, put your `master.key` in `config/`.
* `EDITOR="vi" rails credentials:edit`
* File after edited:

```yaml
production
  secret_key_base: XXXXX
```
