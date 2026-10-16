Analysis helpers
=================

Tools and resources
----------------------

This page is for people using the TIPMIP-ESM data available on DKRZ (Levante).
If you have tools for working with TIPMIP-ESM data that you would like to share, please contact karoline[at]pik-potsdam.de.

.. list-table::
   :header-rows: 1
   :widths: 20 45 35

   * - Issue
     - Solution
     - Notes
   * - 1. It is unclear which data is available on DKRZ and which data the modelling centers will not provide.
     - **Curated list of all variables on DKRZ**, with notes on variables that will not be provided: `spreadsheet <https://docs.google.com/spreadsheets/d/1CvjGE3jYEpcpziwt-5LzBRoCtaLiztAqrHu5YWa7r8w/edit?gid=0#gid=0>`__

       **Variable finder script**: ``python3 /work/bm1448/analysis/karo/tipmip-dkrz-data-processing/dkrz_variable_finder.py <cmip_variable_name>``.
       Add ``-f`` to also print the file paths.
       All options are described in the `README <https://gitlab.pik-potsdam.de/karoline/tipmip-dkrz-data-processing#check-availability-first-with-dkrz-variable-finder>`__.
     - The list is not updated regularly, and some modelling centers did not respond (status: August 2026).
       The script takes some time to run.
   * - 2. There are no model description files for the model versions used here. Separate requests by each user cause a lot of work.
     - **Model specification list**, to be filled in by the modelling centers: `spreadsheet <https://docs.google.com/spreadsheets/d/16LpV8O-zc5l927L7rajtT8URToUO5xEhpp7gpIxBcio/edit?gid=0#gid=0>`__
     - Not all centers have filled it in, but the existing entries are still useful.
   * - 3. Translation of results to temperature space.
     - Method by Jakob Harteg (`jakob.harteg[at]pik-potsdam.de <mailto:jakob.harteg@pik-potsdam.de>`__).
       Code: *(link to be added)*
     - The accompanying paper is in review. The code is already accessible.
   * - 4. Everyone has to do the same basic time series analysis on data with many irregularities.
     - **TIPMIP DKRZ data processing pipeline**: `tipmip-dkrz-data-processing <https://gitlab.pik-potsdam.de/karoline/tipmip-dkrz-data-processing>`__
     - See also the known problems per model.
   * - 5. CESM2 data is not CMORized.
     - **CMORization-light tool** by Karoline Ramin, on Levante at ``/work/bm1448/preESGF/esm/CESM2``.
       Usage is described at the top of ``cesm_data_prep.py``.

       Advantages: simplifies data handling, already in place, available to all Levante users, some experiments are already converted.
     - Limitations: only the metadata of simple variables is converted (not a full CMORization), the method may be imperfect, and only a few people have write access.
       It works only for the simple variables listed in the CESM conversion tab of the `pre-ESGF data request <https://docs.google.com/spreadsheets/d/1VkA2nagWDaZKHgcKEShi8h5Txou3K0kmoNNDGl-TnRs/edit?gid=0#gid=0>`__ (limited access).
       Please contact karoline[at]pik-potsdam.de for problems.
   * - 6. Analysis of abrupt shifts.
     - **TOAD**: *(short description and link to be added by Jakob Harteg)*
     -

