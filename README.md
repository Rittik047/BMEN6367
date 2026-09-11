# BMEN 6367 — Artificial Intelligence in Biomedical Engineering

Coursework repository for BMEN 6367 (The University of Texas at Dallas). It holds the class
notebooks, homework notebooks, and submitted reports for the semester, along with a Google
Drive mirror of the working copies used inside Google Colab.

Author: Rittik Patra · License: MIT

---

## Repository layout

```
BMEN6367/
├── Class Notebooks/                 # notebooks worked through during lecture
│   └── Class1_Aug28.ipynb
├── Homework Notebooks/              # graded notebooks, pushed from Colab
│   ├── Homework1_BMEN6367_Rittik.ipynb
│   └── Homework2_BMEN6367_Rittik.ipynb
├── Homework Submissions/            # written reports handed in alongside the code
│   └── Homework1_BMEN6367_Rittik.docx
├── gdrive/                          # mirror of the MyDrive/BMEN6367 working folder
│   ├── HW1/
│   └── HW2/
│       ├── Homework2_BMEN6367_Rittik.ipynb
│       └── images/                  # head_ct.png, cell_microscopy.png, retina_fundus.png
├── LICENSE
└── README.md
```

Two directory trees hold the same notebooks on purpose. `gdrive/` is a one-way mirror of the
Colab working folder in Google Drive (synced by a cell inside the HW2 notebook), while
`Homework Notebooks/` receives the live, executed state of a notebook pushed directly from the
browser session. If the two ever disagree, `Homework Notebooks/` is the one that was graded.

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
