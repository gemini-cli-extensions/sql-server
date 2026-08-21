# Changelog

## [0.1.7](https://github.com/gemini-cli-extensions/sql-server/compare/0.1.6...0.1.7) (2026-08-21)


### Features

* **groups:** Add ttlMs and cacheScope customization to config ([mcp-toolbox#​3805](https://redirect.github.com/googleapis/mcp-toolbox/issues/3805)) ([a5d4947](https://redirect.github.com/googleapis/mcp-toolbox/commit/a5d49472bad85e8955dc83852e65c5cd92f351a3)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* **migrate:** Convert toolset to group kind during migration ([mcp-toolbox#​3704](https://redirect.github.com/googleapis/mcp-toolbox/issues/3704)) ([0adeaa5](https://redirect.github.com/googleapis/mcp-toolbox/commit/0adeaa51c4e132fe36553b24f88e8f62df90bfaa)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* **server/mcp:** Introduce generic client extension registry ([mcp-toolbox#​3723](https://redirect.github.com/googleapis/mcp-toolbox/issues/3723)) ([016245c](https://redirect.github.com/googleapis/mcp-toolbox/commit/016245c21c254a05409a41845e0a8799518363a0)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* **skill:** Add review-prs skill for mcp-toolbox ([mcp-toolbox#​3743](https://redirect.github.com/googleapis/mcp-toolbox/issues/3743)) ([5b7bacc](https://redirect.github.com/googleapis/mcp-toolbox/commit/5b7bacc73b9284160b73c4c3f7a53214c653e64a)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* **tools:** Add cloud-sql-connect-gce for pg, mysql, mssql ([mcp-toolbox#​3740](https://redirect.github.com/googleapis/mcp-toolbox/issues/3740)) ([ca58fa4](https://redirect.github.com/googleapis/mcp-toolbox/commit/ca58fa4b525d6726b9792a9f6303fbcc26c9ca3f)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* adopt Agent Plugin spec and generate harness manifests ([#99](https://github.com/gemini-cli-extensions/sql-server/issues/99)) ([41190f9](https://github.com/gemini-cli-extensions/sql-server/commit/41190f909defc93aafc9335ec90baeadb667e9fa))


### Bug Fixes

* **auth/mcp:** Derive PRM URL from Toolbox URL ([mcp-toolbox#​3765](https://redirect.github.com/googleapis/mcp-toolbox/issues/3765)) ([aa30842](https://redirect.github.com/googleapis/mcp-toolbox/commit/aa308422ad6dd73a014722c3ebf9628d7aa9cc8f)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* **config:** Ignore environment variables in YAML comments ([mcp-toolbox#​3807](https://redirect.github.com/googleapis/mcp-toolbox/issues/3807)) ([79aa732](https://redirect.github.com/googleapis/mcp-toolbox/commit/79aa73247d35286e1cc4309883d539cf9a470686)), refs [mcp-toolbox#​3793](https://redirect.github.com/googleapis/mcp-toolbox/issues/3793) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* **mcp:** Return Tool execution error for invalid input param ([mcp-toolbox#​3799](https://redirect.github.com/googleapis/mcp-toolbox/issues/3799)) ([8120197](https://redirect.github.com/googleapis/mcp-toolbox/commit/81201978a7a1d2a786eb3707ddaa7b090dd1c454)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* **prebuilt/cloud-storage:** Declare tool collections as groups ([mcp-toolbox#​3764](https://redirect.github.com/googleapis/mcp-toolbox/issues/3764)) ([7d468be](https://redirect.github.com/googleapis/mcp-toolbox/commit/7d468be107dfe476d77bd7f937b5dd9c61e5cdc8)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* **server:** Avoid a nil-flusher panic in the SSE handler ([mcp-toolbox#​3520](https://redirect.github.com/googleapis/mcp-toolbox/issues/3520)) ([947f42f](https://redirect.github.com/googleapis/mcp-toolbox/commit/947f42f3e8a07362466566043045491d2318db29)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* **server/mcp:** Disallow client overriding URL bound parameters ([mcp-toolbox#​3798](https://redirect.github.com/googleapis/mcp-toolbox/issues/3798)) ([f15a9c7](https://redirect.github.com/googleapis/mcp-toolbox/commit/f15a9c7082215bd8e9990395d01b5e4fa3b36c69)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))
* **util:** Convert exponent-form JSON numbers in ConvertNumbers ([mcp-toolbox#​3730](https://redirect.github.com/googleapis/mcp-toolbox/issues/3730)) ([e9713ee](https://redirect.github.com/googleapis/mcp-toolbox/commit/e9713eec3acea912e0b6a254b845bd9da04f8192)) ([735c9fb](https://github.com/gemini-cli-extensions/sql-server/commit/735c9fb8d0e43337d2953bf99882cb8ad53596ea))

## [0.1.6](https://github.com/gemini-cli-extensions/sql-server/compare/0.1.5...0.1.6) (2026-02-24)


### Bug Fixes

* remove broken keychain support for password ([#87](https://github.com/gemini-cli-extensions/sql-server/issues/87)) ([0d096b5](https://github.com/gemini-cli-extensions/sql-server/commit/0d096b5ad677a6c29a710c2ba5a78ba9c55e6ceb))

## [0.1.5](https://github.com/gemini-cli-extensions/sql-server/compare/0.1.4...0.1.5) (2026-01-30)


### Features

* add Configuration settings ([#71](https://github.com/gemini-cli-extensions/sql-server/issues/71)) ([454fd40](https://github.com/gemini-cli-extensions/sql-server/commit/454fd40e1260d52970604b431243b0d02153fc9e))

## [0.1.4](https://github.com/gemini-cli-extensions/sql-server/compare/0.1.3...0.1.4) (2026-01-13)


### Features

* **deps:** update dependency googleapis/mcp-toolbox to v0.25.0 ([#66](https://github.com/gemini-cli-extensions/sql-server/issues/66)) ([7ccba65](https://github.com/gemini-cli-extensions/sql-server/commit/7ccba656ad090805c02200b97b74d449adc963ef))

## [0.1.3](https://github.com/gemini-cli-extensions/sql-server/compare/0.1.2...0.1.3) (2025-12-09)


### Features

* **tool/mssql:** Set default host and port for MSSQL source ([mcp-toolbox#​1943](https://redirect.github.com/googleapis/mcp-toolbox/issues/1943)) ([7a9cc63](https://redirect.github.com/googleapis/mcp-toolbox/commit/7a9cc633768d9ae9a7ff8230002da69d6a36ca86)) ([88756be](https://github.com/gemini-cli-extensions/sql-server/commit/88756bee8851330eb3e3701f10e95f4c7d44476e))

## [0.1.2](https://github.com/gemini-cli-extensions/sql-server/compare/0.1.1...0.1.2) (2025-10-17)


### Features

* **deps:** update dependency googleapis/mcp-toolbox to v0.17.0 ([#32](https://github.com/gemini-cli-extensions/sql-server/issues/32)) ([a72eecf](https://github.com/gemini-cli-extensions/sql-server/commit/a72eecf6fa6e5dc3d7b1b8f2684329c80ecba186))

## [0.1.1](https://github.com/gemini-cli-extensions/sql-server/compare/0.1.0...0.1.1) (2025-09-30)


### Features

* additional instructions for the context file ([#25](https://github.com/gemini-cli-extensions/sql-server/issues/25)) ([effd121](https://github.com/gemini-cli-extensions/sql-server/commit/effd1219f623e8021c5c26eee00e250c04e320c1))
* standardize mcp server names ([#22](https://github.com/gemini-cli-extensions/sql-server/issues/22)) ([383f144](https://github.com/gemini-cli-extensions/sql-server/commit/383f14432c6132efdd5fb8df1d56b34c229ae09e))

## 0.1.0 (2025-09-21)


### Features

* add SQL Server Extension ([cdf0e32](https://github.com/gemini-cli-extensions/sql-server/commit/cdf0e32ab4f93c62f331c9d4817fe0b848232cc8))
