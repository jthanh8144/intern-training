# Package manager

1. What is a Package Manager?
2. Common JavaScript package managers include? npm vs pnpm vs Yarn
3. What is `package.json`?

- dependencies
- devDependencies
- peerDependencies

4. What is `node_modules`?
5. What is `package-lock.json`?
6. `npm install` vs `npm ci`
7. What is Semantic Versioning (SemVer)?
8. Understanding `^` and `~`
9. Understanding the Dependency Tree `npm ls`
10. What is `npm audit`?
11. What is `npx`?
12. Local vs Global Packages
13. Commands You Should Know
```
# Create a project
npm init

# Install a dependency
npm install express

# Install a development dependency
npm install -D typescript

# Remove a dependency
npm uninstall express

# Install dependencies from package.json and the lock file
npm ci

# Run a script
npm run dev

# Inspect dependencies
npm ls

# Check outdated packages
npm outdated

# Check vulnerabilities
npm audit

# View package information
npm view express

# Run a local package CLI
npx tsc

# View npm configuration
npm config list
```
