# EEEIC26---Short-Term-Load-Forecasting-for-Academic-Campi-based-on-DL-and-Feature-Engineering
Complete results of the experiments, with ablation studies on exogenous variables, for short-term load forecasting of an academic campus. Respective of the conference paper submitted to 26th International Conference on Environment and Electrical Engineering by the authors Manuel X. M. Lopes, Carlos Grilo, João Sousa, Pedro Marques and Luís M.N. Távora.

This repository contains a single .xlsx file, "NAME.xlsx", with the results for 24-hour-ahead load profile forecasting and day-ahead forecasting of total daily load (based on aggregation of 24-hour-ahead profile forecasts and day-ahead forecasts based on daily load data).

from docling.document_converter import DocumentConverter  
from docling_core.experimental.serializer.markdown import MarkdownDocSerializer
from docling_core.types.doc import GroupLabel

converter = DocumentConverter()
doc = converter.convert("1D_ahead_results_complete.xlsx").document
serializer = MarkdownDocSerializer(doc=doc)
sheet_md = [serializer.serialize(item=item).text for item in doc.groups if item.label == GroupLabel.SECTION] 
