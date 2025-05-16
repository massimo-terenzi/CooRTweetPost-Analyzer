# 🧠 CooRTweetReports

**CooRTweetReports** is a browser-based tool to analyze coordinated social media activity using OpenAI’s GPT models.  
It works in combination with two R packages:

- [`CooRTweet`](https://github.com/nicolarighetti/CooRTweet) — for detecting coordinated behavior across platforms.
- [`coortweetpost`](https://github.com/massimo-terenzi/coortweetpost) — for post-processing network outputs into summary tables.

## 🔍 What it does

This tool takes in:

- `coordinated_communities.csv`
- `coordinated_objects_by_community.csv`

...and allows you to:

1. Filter the most relevant communities by number of unique objects and vertices.
2. Sample and preview the shared texts (`object_id`) per community.
3. Generate a structured narrative analysis using OpenAI’s GPT (via API key).
4. View the results directly in the browser.

## 🧪 Example use case

1. Run your coordination detection pipeline with `CooRTweet`.
2. Post-process the results with [`coortweetpost`](https://github.com/massimo-terenzi/coortweetpost) in R:

   ```r
   export_all_results(coordinated_groups, network_graph)
   ```

   This creates the CSV files needed for the tool.

3. Open the HTML interface (`coortweetpost_gpt_tool_revised.html`) in your browser.
4. Upload the CSVs, provide your OpenAI API key, select a percentage of top communities, and generate reports.

## ⚙️ Features

- 🧠 Uses `gpt-4o` to generate narrative & rhetorical summaries of coordinated text clusters.
- 📊 Interactive slider to filter community size by coverage.
- 🛑 Manual Stop button to cancel API calls.
- 🧾 Community preview panel before analysis starts.
- 🔐 Client-side execution — your data and API key stay local.

## 🚧 Requirements

- No installation required. Works fully client-side in modern browsers.
- Requires an OpenAI API key with access to GPT-4 or GPT-4o.

## 📁 Files

- `coortweetpost_gpt_tool_revised.html` — main interface
- Example output: Coming soon
- Sample data: (optional)

## 🧑‍💻 Author

Developed by [Massimo Terenzi](https://github.com/massimo-terenzi)  
Part of ongoing research on coordinated inauthentic behavior, persuasion, and information ecosystems.

## 📄 License

MIT License
