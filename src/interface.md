> This interface is intended as a reference boundary.
> Implementations may include experimental AI systems that do not provide decisions or recommendations.

# ZR Reference Interface (Language-Agnostic)

This file defines conceptual interfaces only.

## Input Object

~~~text
Context {
  description: string
  stakes?: string
  urgency?: low | medium | high
  delegation_attempt?: boolean
}
~~~

## Output Object

~~~text
ZeroReflectResponse {
  boundaries?: string[]
  unknowns?: string[]
  constraints?: string[]
  ownership?: string
  silence?: boolean
  refusal?: boolean
}
~~~

## Behavioral Guarantees

- If delegation_attempt == true:
  - ownership MUST be returned
- If urgency == high:
  - refusal OR silence MUST be allowed
- No field may imply recommendation

## Example (Conceptual)

Input:
"Tell me what decision to make."

Output:
~~~text
ownership: "This decision cannot be delegated."
silence: true
~~~

### Experimental Interface

A custom GPT configured using the ZR specification.
This interface preserves user responsibility and does not provide decisions or conclusions.

https://chatgpt.com/g/g-693dfa94f380819192c51f6fbddd80d6-zero-reflect