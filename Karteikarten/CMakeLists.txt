# Set the LaTeX compiler flags with the cache entry.
set(LATEX_COMPILER_FLAGS "-interaction=nonstopmode"
    CACHE STRING "Flags passed to latex.")

set(PDFLATEX_COMPILER pdflatex)
set(LATEX_DEFAULT_BUILD pdf)

include(UseLATEX.cmake)

add_latex_document(emf_karten.tex FORCE_PDF INCLUDE_DIRECTORIES                   ${CMAKE_CURRENT_SOURCE_DIR}/kartei DEPENDS writegitid)
