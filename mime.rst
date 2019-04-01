MIME
====

Linux
-----

No Linux, existe o comando :command:`file` que pode ser utilizado para descrever o tipo MIME de um arquivo. Para isto, basta que se especifique a opção ``--mime-type`` antes de passar o nome do arquivo como argumento. Vejamos um exemplo::

    file --mime-type pythonbasico.pdf

A saída deste comando é: ``application/pdf``

Python
------

Existe uma biblioteca de Python que permite identificar o tipo MIME de um arquivo. Esta biblioteca se chama ``magic``, e não faz parte da biblioteca padrão, isto é, você deverá instalá-la manualmente (Debian/Ubuntu: :command:`sudo apt install -y python3-magic`). No Windows, com o Python já instalado e no caminho de busca de comando (variável *PATH*), execute o comando: :command:`pip install magic`). A página oficial desta biblioteca é: `GitHub - ahupp/python-magic: A python wrapper for libmagic <https://github.com/ahupp/python-magic>`_.

Vejamos um exemplo de código executado no interpretador do Python (Python Shell):

.. code-block:: pycon
   
   >>> import magic
   >>> magic.from_file('pythonbasico.pdf', mime=True)
   'application/pdf'


