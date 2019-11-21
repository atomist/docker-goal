# `atomist/docker-goal`

An Atomist goal to run Docker builds and pushes from an Software
Delivery Machine (SDM).

## Usage

### `docker-build`

This goal runs `docker build` on your project. It does not push the created image.

Put the following YAML into your SDM goal definition to use the `docker-build`
goal.

```yaml
docker_build:

  goals:
  - atomist/docker-goal/docker-build@master:
      input:
      - <specify desired input cache classifiers>
```

### `docker-build-push`

This goal runs `docker build` followed by `docker push`.

Put the following YAML into your SDM goal definition to use the `docker-build-push`
goal.

```yaml
docker_build:

  goals:
  - atomist/docker-goal/docker-build-push@master:
      input:
      - <specify desired input cache classifiers>
```

The `docker-build-push` goal needs credentials to push the Docker image to a
registry. By default the goal will make all Docker registry resource providers
from your Atomist workspace available to the goal. 


## Getting started

See the [Developer Quick Start][atomist-quick] to jump straight to
creating an SDM.

[atomist-quick]: https://docs.atomist.com/quick-start/ (Atomist - Developer Quick Start)

## Contributing

Contributions to this project from community members are encouraged
and appreciated. Please review the [Contributing
Guidelines](CONTRIBUTING.md) for more information. Also see the
[Development](#development) section in this document.

## Code of conduct

This project is governed by the [Code of
Conduct](CODE_OF_CONDUCT.md). You are expected to act in accordance
with this code by participating. Please report any unacceptable
behavior to code-of-conduct@atomist.com.

## Documentation

Please see [docs.atomist.com][atomist-doc] for
[developer][atomist-doc-sdm] documentation.

[atomist-doc-sdm]: https://docs.atomist.com/developer/sdm/ (Atomist Documentation - SDM Developer)

## Connect

Follow [@atomist][atomist-twitter] and [The Composition][atomist-blog]
blog related to SDM.

[atomist-twitter]: https://twitter.com/atomist (Atomist on Twitter)
[atomist-blog]: https://the-composition.com/ (The Composition - The Official Atomist Blog)

## Support

General support questions should be discussed in the `#support`
channel in the [Atomist community Slack workspace][slack].

If you find a problem, please create an [issue][].

[issue]: https://github.com/atomist/docker-goal/issues

---

Created by [Atomist][atomist].
Need Help?  [Join our Slack workspace][slack].

[atomist]: https://atomist.com/ (Atomist - How Teams Deliver Software)
[slack]: https://join.atomist.com/ (Atomist Community Slack)
