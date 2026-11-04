# SWE II Prep Checklist

The pre-start days (Nov 4–8) and Week 1 (Nov 9–15) of the 15-week Software Engineer II study plan. Tick the boxes as you go. This is the same content as the interactive checklist in `index.html`.

---

## Wednesday: tools, accounts and a warm-up

*Nov 4 · 7:00–9:00 PM*

> Running late? Shift every time by the same amount. If time runs short, finish the installs and accounts (up to 8:35 PM) and leave the rest for tomorrow.

### Install your tools

- [ ] **7:00–7:15 PM** Install Python 3.12 or newer from [python.org](https://www.python.org/downloads/). Check it with `python3 --version`. On Windows, tick **Add Python to PATH** during the install.
- [ ] **7:15–7:30 PM** Install [VS Code](https://code.visualstudio.com/) and its **Python** extension (published by Microsoft).
- [ ] **7:30–7:45 PM** Install [Git](https://git-scm.com/downloads) and check it with `git --version`. Then set your identity: `git config --global user.name "Your Name"` and `git config --global user.email "you@example.com"`

### Create your accounts

- [ ] **7:45–8:00 PM** Create a [GitHub](https://github.com) account, or log in to your existing one. Turn on two-factor authentication.
- [ ] **8:00–8:10 PM** Create accounts on [LeetCode](https://leetcode.com) and [neetcode.io](https://neetcode.io). Bookmark the **NeetCode 150** roadmap.
- ☕ **8:10–8:15 PM** Break. Step away from the screen.

### Test that everything works together

- [ ] **8:15–8:25 PM** Create a `python-refresh/` folder and open it in VS Code. Add `hello.py` containing `print("Hello, ShopFlow!")`, then run `python3 hello.py`.
- [ ] **8:25–8:35 PM** Create a `python-refresh` repo on GitHub, then push `hello.py` using the commands GitHub shows you.
- [ ] **8:35–8:40 PM** Create your **error log** with these columns: *Problem, Pattern, What I missed, Key insight*.

### Warm-up

- [ ] **8:40–8:48 PM** LeetCode **Fizz Buzz**
- [ ] **8:48–8:55 PM** LeetCode **Running Sum of 1d Array**
- [ ] **8:55–9:00 PM** Put study time on your calendar: Thursday and Friday 7:00–10:00 PM, and Monday to Friday 7:00–10:00 PM next week.

---

## Thursday: core Python and the interview toolkit

*Nov 5 · 7:00–10:00 PM*

> Stuck on a problem for 8 minutes? Look at a hint, then finish it yourself.

### Syntax tour

- [ ] **7:00–7:25 PM** Work through the first half of [Learn X in Y Minutes: Python](https://learnxinyminutes.com/docs/python/) (primitives, variables, lists, tuples, dicts, sets). Type the examples into `syntax.py` and run them.
- [ ] **7:25–7:50 PM** Do the second half the same way (control flow, functions, classes).
- ☕ **7:50–8:00 PM** Break. Step away from the screen.

### Python for coding interviews

- [ ] **8:00–8:40 PM** Watch NeetCode's **Python for Coding Interviews** video on YouTube. Pause and type each example into `interview.py`.
- [ ] **8:40–9:00 PM** From memory, write one line for each of these, then run them:
  - [ ] Reverse a list using slicing
  - [ ] Sort a list of tuples by their second item, using `key=lambda`
  - [ ] Write a dict comprehension that maps each word to its length
  - [ ] Count the letters in `"banana"` with `Counter`
  - [ ] Group words by their first letter with `defaultdict(list)`
  - [ ] Append and pop from both ends of a `deque`
  - [ ] Push 5 numbers onto a heap with `heapq` and pop the smallest
  - [ ] Loop with `enumerate` and with `zip`
- ☕ **9:00–9:10 PM** Break. Step away from the screen.

### Warm-up problems

- [ ] **9:10–9:20 PM** LeetCode **Reverse String**
- [ ] **9:20–9:30 PM** LeetCode **Valid Palindrome**
- [ ] **9:30–9:40 PM** LeetCode **Majority Element** (try solving it with `Counter`)
- [ ] **9:40–9:50 PM** LeetCode **Missing Number**
- [ ] **9:50–10:00 PM** Update your error log, then save today's files: `git add . && git commit -m "Thursday Python refresh"` and `git push`

---

## Friday: the Python the project needs

*Nov 6 · 7:00–10:00 PM*

### Functions and classes

- [ ] **7:00–7:25 PM** Read the [Python tutorial, section 4.8 onward](https://docs.python.org/3/tutorial/controlflow.html#more-on-defining-functions) (default and keyword arguments, `*args`, `**kwargs`, lambdas). Type out 3 examples.
- [ ] **7:25–7:50 PM** Read the [Python tutorial: Classes](https://docs.python.org/3/tutorial/classes.html), sections 9.3–9.5 only. Then write:
  - [ ] A `Product` class with an `__init__` method and a `__repr__` method
  - [ ] A `DigitalProduct(Product)` subclass that adds a `download_url` attribute
  - [ ] A `@property` called `in_stock` that returns `stock > 0`
- [ ] **7:50–8:00 PM** Explain out loud: *what's the difference between a class and an instance?*
- ☕ **8:00–8:10 PM** Break. Step away from the screen.

### Modern Python features FastAPI uses

- [ ] **8:10–8:30 PM** Read [FastAPI: Python Types Intro](https://fastapi.tiangolo.com/python-types/). Add type hints to your `Product` class.
- [ ] **8:30–8:50 PM** Read the first half of [Real Python: Primer on Python Decorators](https://realpython.com/primer-on-python-decorators/). Then write a `@timer` decorator that prints how long a function took to run.
- [ ] **8:50–9:10 PM** Exceptions:
  - [ ] Write a function that raises `ValueError` when given a negative price
  - [ ] Call it inside `try`/`except`/`finally` and print a friendly error message
  - [ ] Create your own `OutOfStockError(Exception)` class and raise it
- ☕ **9:10–9:15 PM** Break. Step away from the screen.

### Modules, then the self-check

- [ ] **9:15–9:30 PM** Make a `refresh_pkg/` package with `__init__.py`, `models.py` (your Product class) and `main.py` (imports Product and uses it). Run `python3 -m refresh_pkg.main` from the folder that contains `refresh_pkg`.
- [ ] **9:30–9:50 PM** **Self-check.** Write `selfcheck.py` with as few lookups as you can. It should:
  - [ ] Define a `Product` class (name, price, stock) with type hints
  - [ ] Store 4 products in a `dict[int, Product]`
  - [ ] Find the products under $20 with a list comprehension
  - [ ] Count the words in `"the cat and the hat and the bat"` with `Counter`
  - [ ] Raise `ValueError` for a negative price, and catch it
- [ ] **9:50–9:55 PM** Score yourself. 0–2 lookups: you're ready. 3–5: fine, it will come back in Week 1. 6 or more: optionally redo Thursday's Block 2 this weekend (about 1 hour).
- [ ] **9:55–10:00 PM** Save the files: `git add . && git commit -m "Friday Python refresh"` and `git push`

---

## Saturday and Sunday: rest

*Nov 7–8 · Free*

### Rest

- [ ] Nothing planned. Week 1 starts **Monday, Nov 9 at 7:00 PM**.

---

## Ready for Monday when

*Before Nov 9*

> Tick these off before Week 1 starts.

### Checklist

- [ ] Python, VS Code, Git and GitHub all work
- [ ] Your `python-refresh` repo has 3 days of pushes
- [ ] Your error log has entries
- [ ] The self-check script runs
- [ ] Next week's 7:00–10:00 PM sessions are on your calendar

---

## Week 1 · Monday: first endpoint

*Nov 9 · 7:00–10:00 PM*

> Week 1 goal: a small Python API that can create, list, update and delete products, saved on GitHub. Your tools are already installed, so the project starts at the virtual environment.

### LeetCode: arrays and hashing

- [ ] **7:00–8:00 PM** Solve **Contains Duplicate** and **Valid Anagram**. Watch the NeetCode video on [neetcode.io](https://neetcode.io/roadmap) only after a real attempt.
  - [ ] Log anything you missed in your error log
- ☕ **8:00–8:05 PM** Break. Step away from the screen.

### Fundamentals

- [ ] **8:05–8:50 PM** Read [MDN: An overview of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview). The goal: a *client* sends a *request* and a *server* sends back a *response*.

### Project: ShopFlow setup

- [ ] **8:50–9:00 PM** Create a `shopflow` folder and a virtual environment: `python3 -m venv .venv`, then activate it (Mac/Linux: `source .venv/bin/activate`, Windows: `.venv\Scripts\activate`).
- [ ] **9:00–9:10 PM** Install FastAPI: `pip install "fastapi[standard]"`, then `pip freeze > requirements.txt`
- [ ] **9:10–9:25 PM** Create `app/main.py` with a FastAPI app and a `GET /health` endpoint that returns `{"status": "ok"}`. See [FastAPI: First Steps](https://fastapi.tiangolo.com/tutorial/first-steps/).
- [ ] **9:25–9:35 PM** Run `fastapi dev app/main.py`, then open http://127.0.0.1:8000/health and http://127.0.0.1:8000/docs
- [ ] **9:35–9:50 PM** Add a `.gitignore` with `.venv/` and `__pycache__/`. Run `git init`, `git add .`, `git commit -m "Initial FastAPI app"`, create an empty `shopflow` repo on GitHub and push.
- [ ] **9:50–10:00 PM** Explain out loud: what happens between typing a URL and seeing `{"status":"ok"}`?

---

## Week 1 · Tuesday: create and list products

*Nov 10 · 7:00–10:00 PM*

### LeetCode: arrays and hashing

- [ ] **7:00–8:00 PM** Solve **Two Sum** and **Group Anagrams**. Watch the NeetCode video on [neetcode.io](https://neetcode.io/roadmap) only after a real attempt.
  - [ ] Log anything you missed in your error log
- ☕ **8:00–8:05 PM** Break. Step away from the screen.

### Fundamentals

- [ ] **8:05–8:50 PM** Read [MDN: HTTP request methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods) and [MDN: HTTP status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status). Learn **GET, POST, PUT, DELETE** and **200, 201, 204, 400, 404, 422, 500**.

### Project: products

- [ ] **8:50–9:10 PM** Add Pydantic models: `ProductCreate` (name, description, price > 0, stock ≥ 0, using `Field`) and `Product` (adds `id`). See [FastAPI: Request Body](https://fastapi.tiangolo.com/tutorial/body/).
- [ ] **9:10–9:30 PM** Store products in an in-memory `dict[int, Product]`. Add `POST /products` (returns 201) and `GET /products`.
- [ ] **9:30–9:45 PM** Test at `/docs`:
  - [ ] Create 2 or 3 products
  - [ ] List them with GET /products
  - [ ] Send `"price": -5` and see the **422** validation error
- [ ] **9:45–9:50 PM** Commit and push: `git add . && git commit -m "Add create and list products"` then `git push`
- [ ] **9:50–10:00 PM** Explain out loud: why does a negative price return 422 and not 500?

---

## Week 1 · Wednesday: get, update, delete

*Nov 11 · 7:00–10:00 PM*

### LeetCode: arrays and hashing

- [ ] **7:00–8:00 PM** Solve **Top K Frequent Elements** and **Product of Array Except Self**. Watch the NeetCode video on [neetcode.io](https://neetcode.io/roadmap) only after a real attempt.
  - [ ] Log anything you missed in your error log
- ☕ **8:00–8:05 PM** Break. Step away from the screen.

### Fundamentals

- [ ] **8:05–8:50 PM** Read about REST and idempotency on [restfulapi.net](https://restfulapi.net/). Key idea: GET, PUT and DELETE are idempotent, POST is not.

### Project: full CRUD

- [ ] **8:50–9:05 PM** Add `GET /products/{product_id}` that raises `HTTPException(status_code=404)` when the product doesn't exist. See [FastAPI: Handling Errors](https://fastapi.tiangolo.com/tutorial/handling-errors/).
- [ ] **9:05–9:20 PM** Add `PUT /products/{product_id}` to replace a product (404 if missing).
- [ ] **9:20–9:30 PM** Add `DELETE /products/{product_id}` that returns **204** (404 if missing).
- [ ] **9:30–9:45 PM** Test all 5 operations at `/docs`, then create one product from the terminal with `curl -X POST http://127.0.0.1:8000/products -H "Content-Type: application/json" -d '{"name":"Mug","price":12.5,"stock":10}'`
- [ ] **9:45–9:50 PM** Commit and push
- [ ] **9:50–10:00 PM** Explain out loud: what's the difference between PUT and POST, and which one is idempotent?

---

## Week 1 · Thursday: organize the code

*Nov 12 · 7:00–10:00 PM*

### LeetCode: arrays and hashing

- [ ] **7:00–8:00 PM** Solve **Longest Consecutive Sequence**. Watch the NeetCode video on [neetcode.io](https://neetcode.io/roadmap) only after a real attempt.
  - [ ] Log anything you missed in your error log
  - [ ] If time is left, re-solve one problem from your error log
- ☕ **8:00–8:05 PM** Break. Step away from the screen.

### Fundamentals

- [ ] **8:05–8:25 PM** Read the illustrated [How DNS works](https://howdns.works/).
- [ ] **8:25–8:50 PM** Skim [what-happens-when](https://github.com/alex/what-happens-when) for the big picture: DNS, then TCP, then TLS, then the HTTP request and response.

### Project: project structure

- [ ] **8:50–9:00 PM** Create `app/__init__.py`, `app/schemas.py` and `app/routers/__init__.py`, `app/routers/products.py`. See [FastAPI: Bigger Applications](https://fastapi.tiangolo.com/tutorial/bigger-applications/).
- [ ] **9:00–9:10 PM** Move `ProductCreate` and `Product` into `app/schemas.py`
- [ ] **9:10–9:30 PM** Move the product endpoints into `app/routers/products.py` using `APIRouter(prefix="/products", tags=["products"])`. Change paths to `""` and `"/{product_id}"`.
- [ ] **9:30–9:35 PM** In `app/main.py`, keep `/health` and add `app.include_router(products.router)`
- [ ] **9:35–9:45 PM** Write `README.md`: what the project is, how to run it, and the list of endpoints
- [ ] **9:45–9:50 PM** Run the app, confirm everything still works, then commit and push
- [ ] **9:50–10:00 PM** Explain out loud: why split code into schemas and routers instead of one file?

---

## Week 1 · Friday: review and catch up

*Nov 13 · 7:00–10:00 PM*

### LeetCode review

- [ ] **7:00–8:00 PM** Re-solve 2 or 3 problems from your error log **without looking at the solutions**

### Fundamentals review

- [ ] **8:00–8:30 PM** Without notes, answer these out loud:
  - [ ] What happens when I type a URL into the browser and press Enter?
  - [ ] What's the difference between PUT and POST?
  - [ ] What do 201, 404 and 422 mean?
  - [ ] What is idempotency?
  - [ ] Why use a virtual environment?

### Project: finish and document

- [ ] **8:30–9:30 PM** Finish anything left over from this week
- [ ] **9:30–9:50 PM** Create `DECISIONS.md` and write your first entry: why FastAPI (validation, auto docs, async), the alternatives (Flask, Django) and the trade-off
- [ ] **9:50–10:00 PM** Commit and push. Week 1 done 🎉

---

## Week 1 · Weekend: buffer

*Nov 14–15 · Free*

### Buffer

- [ ] Only if you're behind: finish this week's unticked tasks
- [ ] Otherwise rest. Week 2 (moving to PostgreSQL) starts Monday, Nov 16.
