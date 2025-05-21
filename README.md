import OpenAI from 'openai';

const openai = new OpenAI({
  baseURL: 'https://ai.liara.ir/api/v1/682b465e992a7e15e31c6ea0',
  apiKey: '<LIARA_API_KEY>',
});

async function main() {
  const completion = await openai.chat.completions.create({
    model: 'openai/gpt-4o-mini',
    messages: [
      {
        role: 'user',
        content: 'معنای زندگی چیست؟',
      },
    ],
  });

  console.log(completion.choices[0].message);
}

main();
