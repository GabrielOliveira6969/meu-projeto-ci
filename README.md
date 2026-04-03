# Meu Projeto CI

É possível comprovar que os jobs testes-unitarios e scan-de-seguranca executam em paralelo observando a saída do terminal durante a execução do act.

Ambos iniciam após o término do job setup-e-lint e apresentam logs intercalados, indicando execução simultânea.

Além disso, o act cria contêineres Docker distintos para cada job, o que pode ser verificado pelos diferentes IDs de contêiner exibidos no terminal.

Essa execução concorrente ocorre porque ambos possuem a mesma dependência (needs: setup-e-lint) e não dependem entre si.
