# Setting Up Your RFdiffusion CPU-Compatible Fork

## 🚀 **Step-by-Step Fork Setup**

### 1. **Fork the Original Repository**
- Go to [RosettaCommons/RFdiffusion](https://github.com/RosettaCommons/RFdiffusion)
- Click the "Fork" button in the top right
- Choose your GitHub account as the destination

### 2. **Clone Your Fork**
```bash
git clone https://github.com/YOUR_USERNAME/RFdiffusion.git
cd RFdiffusion
```

### 3. **Add Original Repository as Upstream**
```bash
git remote add upstream https://github.com/RosettaCommons/RFdiffusion.git
git remote -v
```

### 4. **Create a New Branch for CPU Patches**
```bash
git checkout -b cpu-compatibility
```

### 5. **Apply the CPU Patches**
The patches are already applied in this repository. They modify:
- `env/SE3Transformer/se3_transformer/model/basis.py`
- `env/SE3Transformer/se3_transformer/model/layers/attention.py`
- `env/SE3Transformer/se3_transformer/model/layers/convolution.py`
- `env/SE3Transformer/se3_transformer/model/layers/norm.py`

### 6. **Update README**
The README has been updated to clearly indicate this is a fork with CPU compatibility patches.

### 7. **Commit and Push**
```bash
git add .
git commit -m "Add CPU compatibility patch for SE3-Transformer"
git push origin cpu-compatibility
```

### 8. **Create Pull Request (Optional)**
- Go to your fork on GitHub
- Click "Compare & pull request"
- This allows others to see your CPU compatibility work

## 🔄 **Keeping Your Fork Updated**

### **Sync with Original Repository**
```bash
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

### **Rebase Your CPU Branch**
```bash
git checkout cpu-compatibility
git rebase main
git push origin cpu-compatibility --force
```

## 📋 **Repository Structure After Fork**

```
rf_diff/
├── README.md              ← Updated with fork notice
├── FORK_SETUP.md          ← This file
├── env/
│   └── SE3Transformer/   ← Patched SE3-Transformer
├── examples/              ← Original examples
├── scripts/               ← Original scripts
└── ... (other original files)
```

## ⚖️ **License and Attribution**

- **Original License**: MIT (from RosettaCommons)
- **Original Authorship**: Rosetta Commons
- **Your Modifications**: CPU compatibility patches
- **Compliance**: Fully compliant with original license

## 🌟 **Benefits of This Approach**

1. **Clear Attribution**: No confusion about original authorship
2. **License Compliance**: Respects original MIT license
3. **Easy Updates**: Can sync with upstream changes
4. **Community Contribution**: Others can find and use your CPU patches
5. **Professional Practice**: Follows open source best practices

## 🎯 **Next Steps**

1. **Push to GitHub**: Share your CPU-compatible version
2. **Document Usage**: Add examples of CPU-only execution
3. **Community Engagement**: Help others who need CPU compatibility
4. **Maintain Updates**: Keep your fork in sync with upstream

---

**Remember**: This fork maintains all the original functionality while adding CPU compatibility. It's a valuable contribution to the community that makes RFdiffusion accessible to more users! 🧬✨
