# LaTeX-builder
A template repo to easily build and release LaTeX documents. Just fork it and use it.

## Usage

The pipeline builds (actions) all *.tex files from the repository root and the pdf files can be downloaded from the artifacts of the build.

The pipeline is running automatically after commits to `main` or `release/*` branches. The same is true for pull requests to those branches.

If a release is generated and published, `main.pdf` is automatically added to the release as `<reponame>_<tagname>.pdf`, e.g., `LaTeX-builder_v0.0.1.pdf`. Therefore, if the release workflow is desired, you need to use `main.tex` as your main LaTeX document.

### Initialization

For the release workflow it is important, that you grant the read/write permissions in Repo-Settings -> Actions -> General -> Workflow permissions

### Version information

The file `section/versinfo.tex` holds version information and it can be included in another .tex file with:
```
\input{section/versinfo.tex}
```

In a normal build it will print `DRAFT ` followed by date and time, e.g. `DRAFT 2023-03-06 13:32:10`.
In a release build it will print the tag name, e.g. v0.0.1.

An example can be found in the `demo.tex` file.

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
