[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=20758079&assignment_repo_type=AssignmentRepo)
# S³ Smart Campus Showcase (Streamlit)
Data-structures-first, semester-long project with a shared dashboard.

## Quick start
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
source .venv/bin/activate
pip install -r requirements.txt

# Run unit tests for the example module
pytest modules/arts_explorer/tests -q

# Launch dashboard
streamlit run app.py
```

### Repo layout
```
app.py
requirements.txt
modules/
  __init__.py
  arts_explorer/
    __init__.py
    ds/
      __init__.py
      sorting.py
      hashmap.py
      queue.py
      stack.py
      heap.py
      bst.py
    ui/
      __init__.py
      page.py
    data/
      sample_events.csv
    tests/
      __init__.py
      test_hashmap.py
      test_queue.py
shared/
  ds_interfaces.py
  utils/
    benchmark.py
.streamlit/
  config.toml
```

### Assignment notes
- Keep UI and data structures separated: UI **imports** your DS; DS must not import Streamlit or pandas.
- Implement your own graded DS (no `dict`/`heapq` for core structures).
- Add your own module under `modules/<your_team>` following the same layout.
