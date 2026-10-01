# BMEN 6367 — Artificial Intelligence in Biomedical Engineering

Coursework repository for BMEN 6367 (The University of Texas at Dallas). It holds the homework
notebooks and submitted reports for the semester, along with a Google Drive mirror of the working
copies used inside Google Colab.

Author: Rittik Patra · License: MIT

---

## Repository layout

```
BMEN6367/
├── Homework Notebooks/              # graded notebooks, pushed from Colab
│   ├── Homework1_BMEN6367_Rittik.ipynb
│   ├── Homework2_BMEN6367_Rittik.ipynb
│   ├── Homework3_BMEN6367_Rittik.ipynb
│   └── Homework4_BMEN6367_Rittik.ipynb
├── Homework Submissions/            # written reports handed in alongside the code
│   ├── Homework1_BMEN6367_Rittik.docx
│   ├── Homework2_BMEN6367_Rittik.docx
│   ├── Homework3_BMEN6367_Rittik.docx
│   └── Homework4_BMEN6367_Rittik.docx
├── gdrive/                          # mirror of the MyDrive/BMEN6367 working folder
│   ├── HW1/
│   │   └── Homework1_BMEN6367_Rittik.ipynb
│   ├── HW2/
│       ├── Homework2_BMEN6367_Rittik.ipynb
│       └── images/                  # head_ct.png, cell_microscopy.png, retina_fundus.png
│   ├── HW3/
│   │   ├── Homework3_BMEN6367_Rittik.ipynb
│   │   └── diabetes.csv
│   └── HW4/
│       └── Homework4_BMEN6367_Rittik.ipynb
├── LICENSE
└── README.md
```

Two directory trees hold the same homework notebooks on purpose. `gdrive/` mirrors the Colab
working folder in Google Drive, while `Homework Notebooks/` stores the submitted, executed
versions used for grading. If the two ever disagree, `Homework Notebooks/` is the grading source.

---

## Running the notebooks

The homework notebooks were developed and executed in Google Colab (Python 3.11) and expect a
mounted Drive. To run them locally instead, remove the `google.colab` cells (Drive mount, token
sync, `cv2_imshow`) and point `IMG_DIR` at `gdrive/HW2/images`.

```bash
git clone https://github.com/Rittik047/BMEN6367.git
cd BMEN6367
python -m venv .venv && source .venv/bin/activate
pip install numpy scipy matplotlib scikit-image networkx pandas opencv-python pillow jupyterlab
jupyter lab
```

`cv2_imshow` is a Colab shim for OpenCV's `imshow`; locally, `plt.imshow` with the channel order
corrected is the direct replacement.

To open a notebook straight in Colab, prefix its GitHub URL with
`https://colab.research.google.com/github/`.


---

## License

MIT — see [LICENSE](LICENSE).
