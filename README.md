# Miget Ubuntu 22 Full Builder

## `miget/builder-ubuntu22-full`

The `miget/builder-ubuntu22-full` image is a squashed clone of the [`paketobuildpacks/builder-jammy-full`](https://github.com/paketo-buildpacks/builder-jammy-full) image, based on Ubuntu 22.04. This image has been created to resolve the specific issue documented in [Issue #556](https://github.com/paketo-buildpacks/builder-jammy-full/issues/556) of the Paketo `paketobuildpacks/builder-jammy-full` repository.

## Purpose
This builder image is designed to provide a consistent environment for building cloud-native applications, with an emphasis on resolving the issues found in the original `paketobuildpacks/builder-jammy-full` image.

## Automatic Updates
A GitHub Actions workflow is configured to periodically check for new releases of the upstream `paketobuildpacks/builder-jammy-full` image. 
When a new version is available, this image is automatically updated to ensure it stays current with upstream improvements.

## Usage

To use this builder in your project, specify it as the builder in your `pack` commands or `project.toml` file:

### `pack`

```
pack build <your-app> --builder miget/builder-ubuntu22-full
```

### `project.toml`

```
[io.buildpacks]
builder = "miget/builder-ubuntu22-full"
```

## Compatibility
This builder is compatible with:

* **Paketo Buildpacks:** Fully supports the same buildpacks as the `paketobuildpacks/builder-jammy-full`.
* **Docker:** Requires Docker to run builds using the builder image.
* **Ubuntu 22.04:** Leverages the latest updates and security patches from Ubuntu 22.04 LTS.

## License
This project is licensed under the same terms as Paketo's original builder. See the [LICENSE](LICENSE) file for more details.