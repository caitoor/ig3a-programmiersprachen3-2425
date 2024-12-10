<script>
  import OpenAI from "openai";

  let haiku = "";

  const config = {
    apiKey: import.meta.env.VITE_OPENAI_API_KEY,
    dangerouslyAllowBrowser: true,
  };

  const openai = new OpenAI(config);

  async function runPrompt() {
    const completion = await openai.chat.completions.create({
      model: "gpt-4o",
      messages: [{ role: "user", content: "write a haiku about ai" }],
    });
    haiku = completion.choices[0].message.content;
    // console.log(completion);
  }

  runPrompt();
</script>

<h1>Your AI haiku:</h1>

{haiku}
