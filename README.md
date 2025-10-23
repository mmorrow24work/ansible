## Sstep-by-step guide to **synchronize your local machine** with your **private GitHub repo** using **SSH**:

---

## 🔧 Step-by-Step: Sync Local Folder with Private GitHub Repo via SSH

### ✅ 1. **Ensure SSH Key Is Set Up and Working**

You've already uploaded your SSH public key to GitHub — now test it:

```bash
ssh -T git@github.com
```

You should see:

```
Hi mmorrow24work! You've successfully authenticated...
```

If that works, you're good to go.

---

### ✅ 2. **Clone the Private Repo Using SSH**

If you haven't cloned it yet:

```bash
git clone git@github.com:mmorrow24work/ansible.git ~/git/ansible
```

This will create a local copy of your private repo in `~/git/ansible`.

---

### ✅ 3. **Work on Your Local Files**

You can now copy or move your playbooks into this repo:

```bash
cp -r /home/mickm/ansible/playbooks/* ~/git/ansible/
cd ~/git/ansible
```

---

### ✅ 4. **Commit and Push Changes**

```bash
git add .
git commit -m "Add playbooks from local machine"
git push origin main
```

> If your repo uses a different branch name (e.g., `master`), replace `main` with that.

---

### ✅ 5. **Keep It in Sync**

Whenever you make changes locally:

```bash
git pull origin main      # Get latest changes
git add .
git commit -m "Your message"
git push origin main      # Push your updates
```

---

Would you like a script to automate syncing your local playbooks to GitHub regularly?
