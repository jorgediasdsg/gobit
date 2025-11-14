GoBIT

Instalar tern
```shell
go install github.com/jackc/tern/v2@latest
```
2. Garantir que o binário está no PATH

Confere onde o Go está colocando os binários:
```shell
go env GOPATH
ls $(go env GOPATH)/bin
```

Se aparecer tern ali, beleza.

Agora, adiciona isso no PATH do zsh (para ficar permanente):
```shell

echo 'export PATH="$PATH:$(go env GOPATH)/bin"' >> ~/.zshrc
source ~/.zshrc
```

Subir o banco (Depois de escrever i migration)
```shell
tern init. /migrations

tern migrate --migrations /migrations --config./migrations/tern.conf

go run /cmd/terndoteny/main.go

brew install sqlc

sqlc generate -f ./internal/store/pgstore/sqlc.yml
```

HotReload
```shell
go install github.com/air-verse/air@latest

air --build.cmd "go build -o ./bin/api ./cmd/api" --build.bin "./bin/api"
```

Criar tabela bom tern
```shell
tern new create_users_table
```