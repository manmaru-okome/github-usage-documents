# github container registryことはじめ

## github container registryとは？

- コンテナイメージを公開・共有できるレジストリサービス
  - docker Hubと同じようなもの
- 自分で作成したイメージを登録しておいて`docker pull`することができる

## コンテナレジストリへのログイン

Macの場合

```bash
$ export CR_PAT={personal access token}
$ echo $CR_PAT | docker login ghcr.io -u {githubユーザー名} --password-stdin
Login Succeeded
```

windowsの場合（**未検証**）

```powershell
> set CR_PAT={personal access token}
> echo %CR_PAT% | docker login ghcr.io -U {githubユーザー名} --password-stdin
Login Succeeded
```

## イメージのプッシュ

```zsh
$ docker pull hello-world
$ docker tag hello-world ghcr.io/{githubユーザー名}/hello-world
$ docker push ghcr.io/{githubユーザー名}/hello-world
Using default tag: latest
The push refers to repository [ghcr.io/manmaru-okome/hello-world]
64df1d35ad6c: Pushed 
latest: digest: sha256:01433e86a06b752f228e3c17394169a5e21a0995f153268a9b36a16d4f2b2184 size: 525
```

## 参考文献

- [Working with the Container registry(公式)](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry)
- [Configuring a package's access control and visibility(公式)](https://docs.github.com/en/packages/learn-github-packages/configuring-a-packages-access-control-and-visibility)
- [GitHub Container Registry 入門](https://www.kaizenprogrammer.com/entry/2020/09/03/060236)
