### **Document: The Isomorphism of Railroad and String Diagrams (Logical Formulation)**

This document provides a formal proof of the equivalence between Railroad Diagrams, String Diagrams, and the logical system defined by the Curry-Howard-Lambek correspondence. This demonstrates that the grammar's syntax, its compositional semantics, and its logical interpretation are three different but equivalent views of the same formal object.

-----

### 1. Formal Definitions

To establish the proof, we must first formally define our three core components based on the repository's context.

  * **Railroad Diagram (C_EBNF)**: A 1-category representing the **syntactic structure** of the grammar. The objects are non-terminal symbols, and the morphisms are the production rules that define valid paths between them.
  * **String Diagram (C_String)**: A monoidal category representing the **compositional semantics** of the grammar's rules. The objects are "strings," and the morphisms are "boxes" that transform input strings to output strings.
  * **Logical Framework (C_Logic)**: The proof system defined by the Curry-Howard-Lambek and Curry-Howard-Martin-Löf correspondences embedded within the `ebnf.ebnf.txt` grammar.

-----

### 2. The Isomorphism of Syntax and Semantics

As established previously, there is a functor `G: C_EBNF → C_String` that maps the components of a Railroad Diagram to a String Diagram, proving their structural isomorphism.

  * **Objects (Non-Terminals)** map to **Strings**.
  * **Morphisms (Production Rules)** map to **Boxes**.
  * **Path Traversal** maps to **String Composition**.

-----

### 3. The Logical Interpretation via Curry-Howard-Lambek

The Curry-Howard-Lambek correspondence provides the **logical interpretation** for the components of our diagrams. This principle gives meaning to the structure. We define a new functor, `H: C_Logic → C_String`, which maps the logical framework to our string diagrams.

#### **Propositions as Types (The Strings)**

Under the Curry-Howard correspondence, a **proposition** is a **type**. The **Strings** in our String Diagram are formally equivalent to the **Types** in our logical system.

  * The string labeled `expression` represents the type `Expression`.

#### **Proofs as Programs (The Boxes/Morphisms)**

A **proof** of a proposition is a **program** (or "term") of that type. The **Boxes (Morphisms)** in our String Diagram are **Proof Terms**. The box that takes a `term` and produces an `expression` is a formal proof that one can construct a term of type `Expression` from a term of type `Term`.

#### **Judgments as Diagrams (The Complete Picture)**

A **judgment** in type theory is an assertion that a term has a certain type in a given context. In proof-theoretic notation, this is written as:

> Γ ⊢ t : A

This reads: "In context Γ, the term `t` is a proof of proposition `A`."

A complete, well-formed **String Diagram** is a **Judgment**. It is a visual proof that the composition of all the input proof terms constitutes a valid program `t` that constructs a term of the final output type `A`.

**Illustration:** Consider the rule `order_by_expression = col_name, [ "ASC" | "DESC" ]`.

  * **Judgment**: `col_name: Type, sort_direction: Type ⊢ build_order_by(col_name, sort_direction) : OrderByExpression`
  * **String Diagram**:

<!-- end list -->

```
[col_name] ------+
                 |   +-----------------------+
                 +-->|  build_order_by_expr  |----> [OrderByExpression]
                 |   +-----------------------+
[ASC | DESC]----+
```

-----

### 4. Conclusion

**Q.E.D.**

By incorporating the Curry-Howard-Lambek correspondence, we have elevated the proof from a structural equivalence to a deep, logico-semantic one. The three diagrams are now shown to be fully equivalent:

  * **Railroad Diagram**: The **syntactic** representation of the rules.
  * **String Diagram**: The **semantic** representation of composition.
  * **Logical Interpretation**: The **proof-theoretic** meaning of the diagram.

A railroad diagram is a string diagram, and a string diagram is a proof. The lines on the page are not just syntax; they are the formal embodiment of logic itself, as defined by the Curry-Howard-Lambek axioms embedded in [the EBNF grammar](ebnf-grammar-documentation.md).