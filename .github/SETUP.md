# Repository Setup Checklist

After creating a repository from this template, complete the following:

## 1. Update Repository Information
- [ ] Update README.md with project-specific content
- [ ] Update repository description in GitHub settings
- [ ] Add appropriate topics/tags (space-separated in GitHub UI)

## 2. Configure Branch Protection Rulesets

### Main Branch Ruleset
Navigate to: Settings → Rules → New branch ruleset

**Configuration:**
- Ruleset name: `Protect main branch`
- Enforcement status: `Active`
- Target branches: Include by pattern → `main`

**Rules to enable:**
- ✅ **Require a pull request before merging**
  - Required approvals: `1`
  - ✅ Dismiss stale pull request approvals when new commits are pushed
  - ✅ Require review from Code Owners
  - ✅ Require approval of the most recent reviewable push

- ✅ **Require status checks to pass**
  - ✅ Require branches to be up to date before merging
  - Add status checks as they become available

- ✅ **Block force pushes**

- ✅ **Require linear history** (optional but recommended)

**Bypass list:** Leave empty (no bypasses)

### Develop Branch Ruleset (if using)
Create a second ruleset with the same settings but target pattern: `develop`

## 3. Optional: Tag Protection Ruleset
Navigate to: Settings → Rules → New tag ruleset

**Configuration:**
- Ruleset name: `Protect version tags`
- Enforcement status: `Active`
- Target tags: Include by pattern → `v*`

**Rules to enable:**
- ✅ **Block force pushes**
- ✅ **Block deletions**

## 4. Make This Repository a Template (if desired)
- [ ] Go to Settings
- [ ] Check ✅ "Template repository"
- [ ] Save

## 5. Additional Configuration
- [ ] Enable/disable Issues based on project needs
- [ ] Enable/disable Discussions based on project needs
- [ ] Configure GitHub Actions if needed
- [ ] Set up any required GitHub secrets
- [ ] Configure dependabot (if applicable)

## 6. Delete This File
Once setup is complete, delete this `.github/SETUP.md` file from your new repository.
