### VS-Lite

#### Requirements

1. UCSF DOCK 6.8
2. AmberTools 17
3. UCSF Chimera

#### Prep in Chimera

1. Open protein / ligand in Chimera
2. Add Hs and charge ligand with Gasteiger
3. Save ligand only as `XXX.ligand.mol2`
4. Add Hs and charge protein with recent AmberFF (to check for missing atoms)
5. Save protein only as `XXX.receptor.pdb`
6. Delete Hs from protein and save again as `XXX.noH.pdb`

### Manual Modifications

May need to make manual modifications to protein / ligand that are only
apparent after encountering errors in this pipeline. Things to look for:

1. Ligand residue name in mol2 file should be `LIG`
2. Ligand atom valences
3. Protein rotamers clash with ligand
4. Protein amino acids missing atoms

### `run.vars.sh`

 Rename `run.vars.sh.example` as `run.vars.sh` and customize to local environment


### `run.001.lig_prep.sh`

Should obtain reasonable `SYS.lig.am1bcc.mol2`. Charge should be correct, atoms
should not have moved.

### `run.002.rec_prep.sh`

Check all `.log` and `.out` files for errors. Open up `SYS.rec.clean.mol2` and
inspect in Chimera. Open up `SYS.lig.am1bcc.mol2` and make sure it is still in
the binding site.



