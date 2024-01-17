# Conventional Commit
This is spec for how I will use Conventional Commit on my commit messages, most of it are inherited from the regular Conventional Commit.
## Partial features
The syntax for it is like this:
```
partial[(<scope>)][!]: <message>

[additional body that this commit partially add n-th features]
```

Usually to put a Work-In-Progress changes to a commit as partial feature.

For example:
```
partial: baseclient implementation
```
```
partial: several implemented features

- authorization
- authentication
- identify
```
```
partial(rpc): allow to use image on RPC
```

## Feature finalization
The syntax looks like this:
```
final[(<scope>)][!]: <message>

[additional body that concludes what this commit do better than the partial features and reference a commit if it contains partial features]
```

Usually to finalize a partial features. You may allow to reuse message if the commit is related to other commit that has partial features.

For example:
```
final: baseclient implementation
```
```
final: several implemented features

this finalized partial features on commit eb42134
```
```
final(rpc): allow to use image in RPC
```