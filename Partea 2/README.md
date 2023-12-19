# Find Median from Data Stream

<details>
<summary>Explicatie</summary>

- Am decis sa utilizez 2 heap-uri de minim respectiv de maxim deoarece asa puteam in cel mai simplu mod sa aflu care este elementul/elementul din mijloc.
- Am folosit heap-ul de maxim sa tin elementele mai mici decat media, iar cel de minim pe cele mai mari.  
    - Cand inserez un element il inserez in heap-ul de maxim daca acesta este mai mic decat radacina acestuia, sau in heapul de minim altfel.
        - Dupa fiecare inserare, "echilibrez" cele 2 heap-uri, daca unul are mai multe elemente decat celalalt, dau pop din el si push in celalalt pana sunt egale. In cazul in care este un numar impar de elemente, aleg sa pastrez cu unul mai mult in heapul de inceput (cel de maxim)
    - Cand trebuie sa aflu media, am 2 cazuri:
        - Cazul in care este un numar par de numere (cele 2 heap-uri sunt egale d.p.d.v. al dimensiunii), In acest caz fac media dintre top-ul de la amandoua.
        - Cazul in care nu au numar egal de elemente, deci este un numar impar de numere, caz in care iau top-ul de la heap-ul de maxim (cel cu primele elemente, cel care in cazul asta are dimensiunea cu 1 mai mare decat celalalt)
- Complexitate:
    - Inserare: O(log n). Deoarece inserez in heap, care are un numar de elemente = n/2
    - Gasire medie: O(1), Deoarece doar iau top-ul de la fiecare, respectiv de la unul din ele, si fac media/ il returnez direct

</details>