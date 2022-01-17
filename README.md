# Iniciar modulo
go mod init goechoweb

# modificar modulo por uno local
go mod edit -replace github.com/labstack/echo/v4=./echo
go mod verify

# eliminar replace
go mod edit -dropreplace github.com/labstack/echo/v4
go mod verify

# empaquetar librerias
go mod vendor

# limpiar librerias no usadas
go mod tidy