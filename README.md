# Yolks

可与翼龙的 Egg 系统(预设)一起使用的精选核心镜像合集。每个镜像都会定期重建，以确保依赖关系始终是最新的。

镜像托管在 `ccr.ccs.tencentyun.com` 上，并存在于 `games`、`installers` 和 `yolks` 空间下。 在确定镜像将位于哪个空间下时使用以下逻辑：

* `oses` — 包含核心包的基础镜像，帮助您入门。
* `games` — 存储库中 `games` 文件夹中的任何内容。这些是为运行特定游戏或游戏类型而构建的镜像。
* `installers` — `installers` 目录中的任何内容。这些镜像将被用于预设的安装脚本使用，而不是用于实际运行游戏服务器。这些镜像仅旨在通预安装常见的安装依赖项（例如 `curl` 和 `wget`）来减少安装时间和额外网络开支。
* `yolks` — 这些是更通用的图像，允许运行不同类型的游戏或脚本。它们通常只是特定版本的软件，并允许翼龙中的不同预设切换使用环境。例如用于运行机器人、Minecraft 服务器等 Java 或 Python 之类的环境。

所有这些镜像都可用于 `linux/amd64` 和 `linux/arm64` 版本，除非另有说明，要在 arm64 系统上使用这些镜像，不需要对它们的标签进行修改，它们应该可以正常工作。

## 贡献

当向现有镜像添加新版本时，例如 `java v42`，您需要将其添加到 `java` 的子文件夹中，例如 `java/42/Dockerfile`。还请更新正确的 `.github/workflows` 文件，以确保正确标记此新版本。

## 可用镜像

### [Oses](/oses)

* [alpine](/oses/alpine)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:alpine`
* [debian](/oses/debian)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:debian`
* [ubuntu](/oses/ubuntu)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:ubuntu`

### [Apps](/apps)

* [`uptimekuma`](/apps/uptimekuma)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:apps_uptimekuma`

### [Bot](/bot)

* [`bastion`](/bot/bastion)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:bot_bastion`
* [`parkertron`](/bot/parkertron)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:bot_parkertron`
* [`redbot`](/bot/red)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:bot_red`
* [`sinusbot`](/bot/sinusbot)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:bot_sinusbot`

### [Box64](/box64)

* [`Box64`](/box64)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:box64`

### [Bun](/bun)

* [`Bun Canary`](/bun/canary)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:bun_canary`
* [`Bun Latest`](/bun/latest)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:bun_latest`

### [Cassandra](/cassandra)

* [`cassandra_java8_python27`](/cassandra/cassandra_java8_python2)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:cassandra_java11_python2`
* [`cassandra_java11_python3`](/cassandra/cassandra_java11_python3)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:cassandra_java11_python3`

### [Dart](/dart)

* [`dart2.17`](/dart/2.17)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dart_2.17`
* [`dart2.18`](/dart/2.18)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dart_2.18`
* [`dart2.19`](/dart/2.19)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dart_2.19`
* [`dart3.3`](/dart/3.3)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dart_3.3`
* [`dart stable`](/dart/stable)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dart_stable`

### [dotNet](/dotnet)

* [`dotnet2.1`](/dotnet/2.1)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dotnet_2.1`
* [`dotnet3.1`](/dotnet/3.1)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dotnet_3.1`
* [`dotnet5.0`](/dotnet/5)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dotnet_5`
* [`dotnet6.0`](/dotnet/6)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dotnet_6`
* [`dotnet7.0`](/dotnet/7)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dotnet_7`
* [`dotnet8.0`](/dotnet/8)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dotnet_8`
* [`dotnet9.0`](/dotnet/9)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:dotnet_9`

### [Elixir](/elixir)

* [`elixir 1.12`](/elixir/1.12)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:elixir_1.12`
* [`elixir 1.13`](/elixir/1.13)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:elixir_1.13`
* [`elixir 1.14`](/elixir/1.14)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:elixir_1.14`
* [`elixir 1.15`](/elixir/1.15)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:elixir_1.15`
* [`elixir latest`](/elixir/latest)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:elixir_latest`

### [Erlang](/erlang)

* [`erlang22`](/erlang/22)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:erlang_22`
* [`erlang23`](/erlang/23)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:erlang_23`
* [`erlang24`](/erlang/24)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:erlang_24`

### [Games](/games)

* [`altv`](/games/altv)
  * `ccr.ccs.tencentyun.com/wapriaily/games:altv`
* [`arma3`](/games/arma3)
  * `ccr.ccs.tencentyun.com/wapriaily/games:arma3`
* [`dayz`](/games/dayz)
  * `ccr.ccs.tencentyun.com/wapriaily/games:dayz`
* [`minetest`](/games/minetest)
  * `ccr.ccs.tencentyun.com/wapriaily/games:minetest`  
* [`mohaa`](games/mohaa)
  * `ccr.ccs.tencentyun.com/wapriaily/games:mohaa`  
* [`Multi Theft Auto: San Andreas`](games/mta)
  * `ccr.ccs.tencentyun.com/wapriaily/games:mta` 
* [`Rust (dedicated server)`](games/rust)
  * `ccr.ccs.tencentyun.com/wapriaily/games:rust`      
* [`samp`](/games/samp)
  * `ccr.ccs.tencentyun.com/wapriaily/games:samp`  
* [`source`](/games/source)
  * `ccr.ccs.tencentyun.com/wapriaily/games:source`
* [`thebattleforwesnoth`](/games/thebattleforwesnoth)
  * `ccr.ccs.tencentyun.com/wapriaily/games:thebattleforwesnoth`
* [`valheim`](/games/valheim)
  * `ccr.ccs.tencentyun.com/wapriaily/games:valheim`

### [Golang](/go)

* [`go1.14`](/go/1.14)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:go_1.14`
* [`go1.15`](/go/1.15)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:go_1.15`
* [`go1.16`](/go/1.16)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:go_1.16`
* [`go1.17`](/go/1.17)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:go_1.17`
* [`go1.18`](/go/1.18)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:go_1.18`
* [`go1.19`](/go/1.19)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:go_1.19`
* [`go1.20`](/go/1.20)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:go_1.20`
* [`go1.21`](/go/1.21)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:go_1.21`
* [`go1.22`](/go/1.22)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:go_1.22`
* [`go1.23`](/go/1.23)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:go_1.23`

### [Java](/java)

* [`java8`](/java/8)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:java_8`
* [`java11`](/java/11)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:java_11`
* [`java16`](/java/16)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:java_16`
* [`java17`](/java/17)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:java_17`
* [`java19`](/java/19)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:java_19`
* [`java21`](/java/21)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:java_21`
* [`java22`](/java/22)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:java_22`

### [MariaDB](/mariadb)

  * [`MariaDB 10.3`](/mariadb/10.3)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mariadb_10.3`
  * [`MariaDB 10.4`](/mariadb/10.4)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mariadb_10.4`
  * [`MariaDB 10.5`](/mariadb/10.5)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mariadb_10.5`
  * [`MariaDB 10.6`](/mariadb/10.6)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mariadb_10.6`
  * [`MariaDB 10.7`](/mariadb/10.7)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mariadb_10.7`
  * [`MariaDB 11.2`](/mariadb/11.2)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mariadb_11.2`
  * [`MariaDB 11.3`](/mariadb/11.3)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mariadb_11.3`
  * [`MariaDB 11.4`](/mariadb/11.4)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mariadb_11.4`
  * [`MariaDB 11.5`](/mariadb/11.5)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mariadb_11.5`
  * [`MariaDB 11.6`](/mariadb/11.6)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mariadb_11.6`

### [MongoDB](/mongodb)

  * [`MongoDB 4`](/mongodb/4)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mongodb_4`
  * [`MongoDB 5`](/mongodb/5)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mongodb_5`
 * [`MongoDB 6`](/mongodb/6)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mongodb_6`    
 * [`MongoDB 7`](/mongodb/7)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mongodb_7`
 * [`MongoDB 8`](/mongodb/8)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:mongodb_8`

### [Mono](/mono)

* [`mono_latest`](/mono/latest)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:mono_latest`

### [Nodejs](/nodejs)

* [`node12`](/nodejs/12)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_12`
* [`node14`](/nodejs/14)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_14`
* [`node16`](/nodejs/16)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_16`
* [`node17`](/nodejs/17)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_17`
* [`node18`](/nodejs/18)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_18`
* [`node19`](/nodejs/19)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_19`
* [`node20`](/nodejs/20)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_20`
* [`node21`](/nodejs/21)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_21`
* [`node22`](/nodejs/22)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_22`
* [`node23`](/nodejs/23)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_23`
* [`node24`](/nodejs/24)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:nodejs_24`

### [PostgreSQL](/postgres)

  * [`Postgres 9`](/postgres/9)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:postgres_9`
  * [`Postgres 10`](/postgres/10)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:postgres_10`
  * [`Postgres 11`](/postgres/11)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:postgres_11`
  * [`Postgres 12`](/postgres/12)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:postgres_12`
  * [`Postgres 13`](/postgres/13)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:postgres_13`
  * [`Postgres 14`](/postgres/14)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:postgres_14`  

### [Python](/python)

* [`python3.7`](/python/3.7)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:python_3.7`
* [`python3.8`](/python/3.8)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:python_3.8`
* [`python3.9`](/python/3.9)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:python_3.9`
* [`python3.10`](/python/3.10)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:python_3.10`
* [`python3.11`](/python/3.11)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:python_3.11`
* [`python3.12`](/python/3.12)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:python_3.12`
* [`python3.13`](/python/3.13)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:python_3.13`

### [Redis](/redis)

  * [`Redis 5`](/redis/5)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:redis_5`
  * [`Redis 6`](/redis/6)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:redis_6`
  * [`Redis 7`](/redis/7)
    * `ccr.ccs.tencentyun.com/wapriaily/yolks:redis_7`

### [Rust](/rust)

* [`rust1.56`](/rust/1.56)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:rust_1.56`
* [`rust1.60`](/rust/1.60)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:rust_1.60`
* [`rust latest`](/rust/latest)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:rust_latest`

### [SteamCMD](/steamcmd)
* [`SteamCMD Debian lastest`](/steamcmd/debian)
  * `ccr.ccs.tencentyun.com/wapriaily/steamcmd:debian`
* [`SteamCMD Debian Dotnet`](/steamcmd/dotnet)
  * `ccr.ccs.tencentyun.com/wapriaily/steamcmd:dotnet`
* [`SteamCMD Proton`](/steamcmd/proton)
  * `ccr.ccs.tencentyun.com/wapriaily/steamcmd:proton`
* [`SteamCMD Proton`](/steamcmd/proton_8)
  * `ccr.ccs.tencentyun.com/wapriaily/steamcmd:proton_8`
* [`SteamCMD Sniper latest`](/steamcmd/sniper)
  * `ccr.ccs.tencentyun.com/wapriaily/steamcmd:sniper`
* [`SteamCMD Ubuntu latest LTS`](/steamcmd/ubuntu)
  * `ccr.ccs.tencentyun.com/wapriaily/steamcmd:ubuntu`

### [Voice](/voice)
* [`Mumble`](/voice/mumble)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:voice_mumble`
* [`TeaSpeak`](/voice/teaspeak)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:voice_teaspeak`

### [Wine](/wine)

* [`Wine`](/wine)
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:wine_7`
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:wine_8`
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:wine_9`
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:wine_10`
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:wine_latest`
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:wine_devel`
  * `ccr.ccs.tencentyun.com/wapriaily/yolks:wine_staging`

### [Installation Images](/installers)

* [`alpine-install`](/installers/alpine)
  * `ccr.ccs.tencentyun.com/wapriaily/installers:alpine`
* [`debian-install`](/installers/debian)
  * `ccr.ccs.tencentyun.com/wapriaily/installers:debian`
* [`ubuntu-install`](/installers/ubuntu)
  * `ccr.ccs.tencentyun.com/wapriaily/installers:ubuntu`
