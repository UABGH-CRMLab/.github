# C. Ryan Miller Lab @ UAB

**Gliomas | Molecular Neuropathology | Kinome | Signal Transduction | Experimental Therapeutics | Genomics | Bioinformatics | Computational Biology**

Welcome to the GitHub organization for the research laboratory of C. Ryan Miller, MD, PhD (CRM) at the University of Alabama at Birmingham. We develop and maintain open-source tools for bioinformatics workflows and cancer genomics research.

---

## 🧬 Infrastructure Repositories

### [crmlabBioStack](https://github.com/UABGH-CRMLab/crmlabBioStack)
**Bioinformatics Development Container**

Docker container optimized for genomics analysis with RStudio Server, R 4.5.1, Bioconductor 3.21, and 111+ pre-installed packages. Provides a reproducible environment for all lab analysis workflows.

**Includes:**
- 🔧 RStudio Server with web interface
- 📊 Data science stack (tidyverse, data.table, Seurat)
- 🧬 Bioconductor genomics packages (DESeq2, clusterProfiler, edgeR)
- 🐍 Python with Streamlit for interactive apps
- 📈 Visualization tools (ggplot2, ComplexHeatmap, pheatmap)
- ✅ CI/CD testing for image builds and package availability

**Quick Start:**
```bash
docker pull uabcrmlab/crmlabbiostack:2.5
docker run -d -p 8787:8787 -e PASSWORD=yourpassword uabcrmlab/crmlabbiostack:2.5
```

**Latest Version:** v2.5 - Production Release
**Links:** [GitHub Repository](https://github.com/UABGH-CRMLab/crmlabBioStack) • [Docker Hub](https://hub.docker.com/r/uabcrmlab/crmlabbiostack)

---

### [crmlabBulkRNA](https://github.com/UABGH-CRMLab/crmlabBulkRNA)
**RNA-seq Analysis Template**

Production-grade template combining DESeq2 differential expression with clusterProfiler GSEA enrichment analysis. Processes Salmon quantifications through a modular R/RMarkdown architecture with automated MSigDB integration.

**Features:**
- 🔬 Multi-factor experimental designs (factorial, interaction models)
- 📊 Comprehensive QC and visualization suite
- 🧪 Automated gene set enrichment (GSEA/ORA)
- 🐭 Multi-species support (human, mouse)
- ⚡ High-performance parallel processing
- 📦 Reproducible analysis reports
- ✅ CI/CD validation for template structure and R syntax

**Latest Release:** [v1.1](https://github.com/UABGH-CRMLab/crmlabBulkRNA/releases/latest) - Standardized Infrastructure

---

### [crmlabDB](https://github.com/UABGH-CRMLab/crmlabDB)
**Lab Database and Shiny Interface**

SQLite database with Shiny web interface for managing experimental metadata, sample tracking, and analysis results.

**Features:**
- 🗄️ SQLite database for lab data management
- 📱 Interactive Shiny web interface
- 🔍 Sample and experiment tracking
- 📊 Analysis results integration
- ✅ CI/CD testing for database integrity and Shiny app

---

### [crmlabAnnoHub](https://github.com/UABGH-CRMLab/crmlabAnnoHub)
**Gene Set Annotation Hub**

Curated collection of gene sets and annotation resources for pathway analysis and functional enrichment.

**Features:**
- 📚 Curated gene set collections (GMT format)
- 🧬 Multi-species gene annotations
- 🔄 Export and import functionality
- ✅ CI/CD validation for gene set format and duplicates

---

### [crmlabWorkspace](https://github.com/UABGH-CRMLab/crmlabWorkspace)
**Multi-Repository Development Workspace**

VSCode workspace configuration for unified development across all lab infrastructure repositories.

**Features:**
- 📁 Multi-root workspace for seamless navigation
- 🔧 Shared development tools and settings
- 📖 Comprehensive documentation and onboarding guides
- 🤖 GitHub Copilot integration
- ✅ CODEOWNERS for automated code review

---

## 🚀 Getting Started

### For Lab Members (Full Development Environment)

1. **Clone the workspace and all repositories:**
   ```bash
   cd /data
   git clone https://github.com/UABGH-CRMLab/crmlabWorkspace.git
   git clone https://github.com/UABGH-CRMLab/crmlabBioStack.git
   git clone https://github.com/UABGH-CRMLab/crmlabBulkRNA.git
   git clone https://github.com/UABGH-CRMLab/crmlabDB.git
   git clone https://github.com/UABGH-CRMLab/crmlabAnnoHub.git
   ```

2. **Open the multi-root workspace in VSCode:**
   ```bash
   code crmlabWorkspace/crmlabWorkspace.code-workspace
   ```

3. **See the [Developer Onboarding Guide](https://github.com/UABGH-CRMLab/crmlabWorkspace/blob/main/docs/DEVELOPER_ONBOARDING.md)** for complete setup instructions

### For External Users (RNA-seq Analysis Only)

1. **Clone the RNA-seq template:**
   ```bash
   git clone https://github.com/UABGH-CRMLab/crmlabBulkRNA.git
   cd crmlabBulkRNA
   ```

2. **Start the Docker container:**
   ```bash
   docker run -d -p 8787:8787 \
     -v $(pwd):/data/crmlabBulkRNA \
     -e PASSWORD=rstudio \
     uabcrmlab/crmlabbiostack:2.5
   ```

3. **Access RStudio:** Navigate to `http://localhost:8787` (user: `rstudio`)

4. **Configure your analysis:** Edit `config/config.yaml` with your experimental design

5. **Run analysis:** Open `crmlabBulkRNA.Rmd` in RStudio and knit

---

## 📚 Documentation

- **Workspace Documentation:**
  - [Developer Onboarding Guide](https://github.com/UABGH-CRMLab/crmlabWorkspace/blob/main/docs/DEVELOPER_ONBOARDING.md) - Get started with the lab environment
  - [Multi-Repo Workflow](https://github.com/UABGH-CRMLab/crmlabWorkspace/blob/main/docs/MULTI_REPO_WORKFLOW.md) - Working across repositories
  - [Wiki Templates](https://github.com/UABGH-CRMLab/crmlabWorkspace/wiki) - Documentation and knowledge base

- **RNA-seq Template:**
  - [README](https://github.com/UABGH-CRMLab/crmlabBulkRNA/blob/main/README.md) - Overview and quick start
  - [Function Reference](https://github.com/UABGH-CRMLab/crmlabBulkRNA/blob/main/FUNCTION_REFERENCE.md) - Complete function documentation
  - [Configuration Guide](https://github.com/UABGH-CRMLab/crmlabBulkRNA/blob/main/config/config_template.yaml) - Experimental design setup

- **Docker Container:**
  - [README](https://github.com/UABGH-CRMLab/crmlabBioStack/blob/main/README.md) - Container overview and version history
  - [Docker Hub](https://hub.docker.com/r/uabcrmlab/crmlabbiostack) - Official images

---

## 🔬 Research Focus

Our lab develops computational infrastructure and workflows for:

- **RNA-seq Analysis:** Differential expression, gene set enrichment, pathway analysis
- **Cancer Genomics:** Driver mutations, tumor heterogeneity, therapeutic targets in gliomas
- **Signal Transduction:** Kinome analysis and pathway activation
- **Molecular Neuropathology:** Brain tumor classification and biomarker discovery
- **Reproducible Research:** Docker containers, automated workflows, version-controlled analyses

---

## 🤝 Contributing

We welcome contributions! All infrastructure repositories use:

- **Branch Protection:** All changes to `main` require pull requests
- **Code Review:** CODEOWNERS automatically request reviews from maintainers
- **CI/CD Testing:** Automated workflows validate code before merge
- **Documentation:** Clear README files and inline documentation required

For lab members, see the [Developer Onboarding Guide](https://github.com/UABGH-CRMLab/crmlabWorkspace/blob/main/docs/DEVELOPER_ONBOARDING.md).

External contributors should open issues to discuss changes before submitting PRs.

---

## 📧 Contact

**C. Ryan Miller, MD, PhD**  
University of Alabama at Birmingham  
Birmingham, AL 35294  

For questions, bug reports, or collaboration inquiries, please open an issue in the relevant repository.

---

## 📄 License

All software is released under the MIT License unless otherwise specified. See individual repository LICENSE files for details.

---

## 🏷️ Latest Releases

| Repository | Version | Release Date | Notes |
|-----------|---------|--------------|-------|
| [crmlabBioStack](https://github.com/UABGH-CRMLab/crmlabBioStack) | v2.5 | 2026-02-05 | Production release with CI/CD |
| [crmlabBulkRNA](https://github.com/UABGH-CRMLab/crmlabBulkRNA) | v1.1 | 2026-02-05 | Infrastructure standardization |
| [crmlabDB](https://github.com/UABGH-CRMLab/crmlabDB) | v1.1 | 2026-02-05 | Database with Shiny interface |
| [crmlabAnnoHub](https://github.com/UABGH-CRMLab/crmlabAnnoHub) | v1.1 | 2026-02-05 | Gene set annotation hub |
| [crmlabWorkspace](https://github.com/UABGH-CRMLab/crmlabWorkspace) | v1.1 | 2026-02-05 | Multi-repo workspace |
