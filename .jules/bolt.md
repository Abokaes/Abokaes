## 2025-05-15 - Optimizing CI for Minimalist Repositories
**Learning:** In repositories primarily used for documentation or GitHub Profiles, standard CI templates often run on every push, even for non-functional README updates. This wastes CI minutes and can lead to a backlog of redundant runs.
**Action:** Always implement `paths-ignore` for documentation and `concurrency` with `cancel-in-progress: true` to ensure CI only runs when necessary and never blocks with redundant builds.
