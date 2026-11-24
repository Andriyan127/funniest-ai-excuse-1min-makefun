# Test

## How it was verified

1. Ran the program with an explicit output dir:
   ```sh
   MAKEFUN_OUTPUT_DIR=/tmp/makefun-test-output node main.ts
   ```
2. Ran it again with the default output dir:
   ```sh
   node main.ts   # writes /output/entry.txt
   ```
3. Checked the output file:
   ```sh
   wc -c /output/entry.txt
   # 74 /output/entry.txt
   cat /output/entry.txt
   # I called the deadline-checking tool 4,000 times. It kept answering 'soon.'
   ```
4. Confirmed byte-exactness with Python: the file's 74 bytes equal the
   winning line encoded as UTF-8, with **no trailing newline** and **no
   embedded newline** (single line).

## Results

- `entry.txt` contains exactly the winning line: 74 characters, within the
  1–200 character gate, plain UTF-8, one line.
- No dependencies; `node main.ts` exits 0 in both runs.
- Node version used: v24.22.1.
