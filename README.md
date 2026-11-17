# EC&EE Machine · PT

Classroom quizzes for **Conforto Ambiental e Eficiência Energética / Environmental Comfort and Energy Efficiency**,
Lisbon School of Architecture (Faculdade de Arquitetura, Universidade de Lisboa).

Live: https://ncorticos.github.io/ec-ee-machine-pt/ (the Course Book opens it from the Machine tab).

A clean copy of [EC&EE Machine](https://github.com/ncorticos/ec-ee-machine) 1.30.0, which now serves Warsaw (SGGW):

- Lisbon only, PT and EN, Theoretical quizzes only (no LAB submissions).
- No lecture is closed; no attempts or results carried over.
- 1252 questions: the 1383 of the original bank without the 131 specific to Poland.
- Its own results Worker, `quiz-results-pt` (`worker.js`, `wrangler.toml`), writing to its own private results repository.
- Device storage under its own keys, so a shared computer never shows Warsaw history here.

## Results Worker setup (Cloudflare)

1. Workers & Pages > Create > Import a repository > `ncorticos/ec-ee-machine-pt`, name `quiz-results-pt`.
2. Settings > Variables and Secrets: `REPO` = `ncorticos/quiz-results-pt`, `CLASS_CODE` (comma-separated class codes),
   secrets `GITHUB_TOKEN` (fine-grained, contents read/write on `quiz-results-pt` only) and `TEACHER_CODE`.
3. Deploy. The page sends results to `https://quiz-results-pt.ncorticos.workers.dev`.
