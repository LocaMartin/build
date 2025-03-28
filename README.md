# go-build

- create repo in github clone it to local machine
```bash
git clone https://github.com/LocaMartin/turtle
```
- write code `Go` code

- Create a `go.mod` file:
```bash
go mod init github.com/LocaMartin/turtle
```

```bash
go mod tidy
```
- add workflow file
  
```
.github/workflow/workflow.yaml
```
- Make initial push
```bash
git add .
```

```bash
git commit -m "initial push"
```

```bash
git push origin main --tags
```

```bash
# Semantic versioning format (vMAJOR.MINOR.PATCH)
git tag -a v1.0.0 -m "Initial release version 1.0.0"
```

```bash
# Push code and tags
git push origin main --tags
```
- Verify Tags
```
# List local tags
git tag

# List remote tags
git ls-remote --tags origin
```

**Update Process for New Versions**
- Commit code changes
- Create new tag:
```bash
git tag -a v1.0.1 -m "Add file validation feature"
```
- Push with tags
```
git push origin main --tags
```
- Delete a Tag (if needed)
```bash
# Delete local tag
git tag -d v1.0.0

# Delete remote tag
git push origin --delete v1.0.0
```

**Semantic Versioning Format:**

- v<MAJOR>.<MINOR>.<PATCH>
Example: **`v1.2.3`**

    - MAJOR: Breaking changes

    - MINOR: New features (backwards compatible)

    - PATCH: Bug fixes

- Annotated Tags (-a flag):

  -  Store author info

  -  Have timestamp

  -  Recommended for releases

- When You Need GitHub Actions Workflow:

  - Automated Testing
  - Run go test on every push/pull request
  - Cross-platform Builds
  - Compile binaries for Windows/Linux/macOS automatically
  - Release Automation
  - Create GitHub releases when you push tags
  - Code Quality Checks
  - Enforce formatting (gofmt), linting (golint), or security scans
  - Dependency Updates
  - Automate Go module dependency management

- When You Don't Need It:

  - Small personal projects
  - Early development stages
  - Manual testing/building is acceptable
  - No multi-platform distribution needed
