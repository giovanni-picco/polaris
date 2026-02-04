# FluxCD

Setup of the Flux system within the cluster.
This is my personal implementation and understanding of the installation workflow described in the official [FluxCD documentation](https://fluxcd.io/).

## Installation

1. Obtain a GitHub PAT (Personal Access Token).
   You can generate or regenerate one from the [GitHub Personal Access Tokens](https://github.com/settings/personal-access-tokens/) page.
   Once generated, export it as an environment variable:

    ```sh
    export GITHUB_TOKEN=<gh-token>
    ```

2. Install the Flux CLI by following the procedure described [here](https://fluxcd.io/flux/installation/#install-the-flux-cli).

3. Run the `bootstrap` command. Example:

    ```sh
    flux bootstrap github \
        --token-auth \
        --owner=giovanni-picco \
        --repository=polaris \
        --branch=feature/test \
        --path=k8s/flux \
        --personal
    ```
