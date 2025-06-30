# Changesets Java Dependabot GitHub Action
A GitHub Action that automatically creates a changeset for Java dependencies that are updated by Dependabot. It uses the [changesets-java Maven plugin](https://github.com/FortnoxAB/changesets-java) to generate the changeset file.


```yaml
steps:
- uses: actions/checkout@v4
- uses: FortnoxAB/changesets-java-dependabot-action@main
```

By default, the action expects to find Maven Wrapper in the root of the repository. If you use something else or want to specify a different path, you can set the `maven-executable` input:

```yaml
steps:
- uses: actions/checkout@v4
- uses: FortnoxAB/changesets-java-dependabot-action@main
  with:
    maven-executable: mvn
```


## To do
- Add a changelog
- Release a version and keep the README up to date. There must be some fancy automation to use for this :)
