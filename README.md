# C. Ryan Miller Lab at UAB

**Bioinformatics | Genomics | Computational Biology | Signal Transduction | Molecular Pathology | Gliomas**

Welcome to the GitHub organization for the C. Ryan Miller (CRM) Lab at the University of Alabama at Birmingham (UAB). We develop and maintain open-source tools for RNA-seq analysis, bioinformatics workflows, and cancer genomics research.

---

## 🧬 Featured Projects

### [bRNA3F](https://github.com/UABGH-CRMLab/bRNA3F)
**Enterprise RNA-seq Analysis Pipeline**

Production-grade template combining DESeq2 differential expression with clusterProfiler GSEA enrichment analysis. Processes Salmon quantifications through a modular R/RMarkdown architecture with automated MSigDB integration.

**Features:**
- 🔬 Multi-factor experimental designs (factorial, interaction models)
- 📊 Comprehensive QC and visualization suite
- 🧪 Automated gene set enrichment (GSEA/ORA)
- 🐭 Multi-species support (human, mouse)
- ⚡ High-performance parallel processing
- 📦 Reproducible analysis reports

**Latest Release:** [v5.9.0](https://github.com/UABGH-CRMLab/bRNA3F/releases/latest) - Validation Framework & Date Consistency

---

### [250829_rstudio](https://github.com/UABGH-CRMLab/250829_rstudio)
**RStudio Development Container**

Docker container optimized for bioinformatics and genomics analysis with RStudio Server, R 4.5.1, Bioconductor 3.21, and 111+ pre-installed packages.

**Includes:**
- 🔧 RStudio Server with web interface
- 📊 Data science stack (tidyverse, data.table, Seurat)
- 🧬 Bioconductor genomics packages (DESeq2, clusterProfiler, edgeR)
- 🐍 Python with Streamlit for interactive apps
- 📈 Visualization tools (ggplot2, ComplexHeatmap, pheatmap)

**Quick Start:**
```bash
docker pull uabcrmlab/250829_rstudio:latest
docker run -d -p 8787:8787 -e PASSWORD=yourpassword uabcrmlab/250829_rstudio:latest
```

**Latest Version:** [v2.4](https://hub.docker.com/r/uabcrmlab/250829_rstudio) - Streamlit Integration

---

## 🚀 Getting Started

### For RNA-seq Analysis

1. **Clone the template:**
   ```bash
   git clone https://github.com/UABGH-CRMLab/bRNA3F.git
   cd bRNA3F
   ```

2. **Start development container:**
   ```bash
   docker run -d -p 8787:8787 \
     -v $(pwd):/data/bRNA3F \
     -e PASSWORD=rstudio \
     uabcrmlab/250829_rstudio:latest
   ```

3. **Access RStudio:** Navigate to `http://localhost:8787` (user: `rstudio`)

4. **Configure your analysis:** Edit `config/config.yaml` with your experimental design

5. **Run analysis:**
   ```bash
   Rscript -e 'rmarkdown::render("run_analysis.Rmd")'
   ```

---

## 📚 Documentation

- **bRNA3F Documentation:**
  - [README](https://github.com/UABGH-CRMLab/bRNA3F/blob/main/README.md) - Overview and quick start
  - [Configuration Guide](https://github.com/UABGH-CRMLab/bRNA3F/blob/main/config/CONFIG_GUIDE.md) - Experimental design setup
  - [Configuration Reference](https://github.com/UABGH-CRMLab/bRNA3F/blob/main/config/CONFIGURATION_REFERENCE.md) - Complete settings documentation

- **Docker Container:**
  - [Getting Started](https://github.com/UABGH-CRMLab/250829_rstudio/blob/main/GETTING_STARTED.md)
  - [Version History](https://github.com/UABGH-CRMLab/250829_rstudio/blob/main/README.md#version-history)

---

## 🔬 Research Focus

Our lab develops computational methods and workflows for:

- **RNA-seq Analysis:** Differential expression, gene set enrichment, pathway analysis
- **Cancer Genomics:** Driver mutations, tumor heterogeneity, therapeutic targets
- **Single-Cell Analysis:** Cell type identification, trajectory inference, marker discovery
- **Multi-omics Integration:** Combining transcriptomics, genomics, and proteomics data

---

## 🤝 Contributing

We welcome contributions! Please see individual repository CONTRIBUTING.md files for guidelines.

**Code of Conduct:** All repositories follow our [Code of Conduct](https://github.com/UABGH-CRMLab/bRNA3F/blob/main/CODE_OF_CONDUCT.md).

---

## 📧 Contact

**Miller Lab**
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
| [bRNA3F](https://github.com/UABGH-CRMLab/bRNA3F/releases/latest) | v5.9.0 | 2026-01-10 | Validation framework & hardcoding audit |
| [250829_rstudio](https://github.com/UABGH-CRMLab/250829_rstudio/releases/latest) | v2.4 | 2026-01-02 | Streamlit integration |

---

<div align="center">

**[Repositories](https://github.com/orgs/UABGH-CRMLab/repositories)** • **[Docker Hub](https://hub.docker.com/u/uabcrmlab)** • **[UAB O'Neal Comprehensive Cancer Center](https://www.uab.edu/onealcancercenter/)**

</div>
